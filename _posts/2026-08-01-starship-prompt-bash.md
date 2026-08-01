---
layout: post
title:  "Configuring the Starship Prompt for Bash"
date:   2026-08-01 12:00:00 -0700
categories: [Linux]
---

[Starship](https://starship.rs) is a minimal, fast, and highly customizable shell prompt written in Rust. It works the same way across Bash, Zsh, Fish, PowerShell, and more, so you only need to learn one configuration format no matter which shell you end up using. Here's how to install it and set it up for Bash.

### Installing Starship

The quickest way to install Starship on Linux/macOS is via its install script:

{% highlight shell %}
curl -sS https://starship.rs/install.sh | sh
{% endhighlight %}

This drops a single `starship` binary onto your `PATH` (e.g. `/usr/local/bin/starship`). Verify it worked with:

{% highlight shell %}
starship --version
{% endhighlight %}

### Enabling it in Bash

Starship doesn't do anything until your shell's init script asks it to render the prompt. Add this line near the end of `~/.bashrc`:

{% highlight shell %}
eval "$(starship init bash)"
{% endhighlight %}

Open a new terminal (or run `source ~/.bashrc`) and you should immediately see the default Starship prompt.

### Configuring `~/.config/starship.toml`

Starship reads its configuration from `~/.config/starship.toml`. Here's a config that trims the prompt down to what actually matters day-to-day: current directory, git status, a colored success/error indicator, and a right-aligned command duration/clock.

{% highlight toml %}
"$schema" = 'https://starship.rs/config-schema.json'

add_newline = true
right_format = """$cmd_duration$time"""

[character]
success_symbol = '[❯](bold green)'
error_symbol = '[❯](bold red)'

[directory]
truncation_length = 3
truncate_to_repo = true

[git_status]
ahead = '⇡${count}'
behind = '⇣${count}'
diverged = '⇕⇡${ahead_count}⇣${behind_count}'
staged = '+${count}'
modified = '!${count}'
untracked = '?${count}'
stashed = '${count}'

[cmd_duration]
min_time = 2000
format = 'took [$duration]($style) '

[time]
disabled = false
format = '[$time]($style)'
time_format = '%H:%M'
style = 'bold dimmed white'
{% endhighlight %}

A few notes on what each section does:

- `$schema` points editors like VS Code at Starship's JSON schema, giving you autocomplete and validation while editing the file.
- `add_newline` puts a blank line before each prompt, which keeps a busy terminal easier to scan.
- `[character]` swaps the default `➜` for a simple arrow (`❯`) that turns green on success and red after a failed command — an easy way to spot a bad exit code at a glance.
- `[directory]` truncates long paths to the last 3 segments, and `truncate_to_repo` shows the path relative to the repository root when you're inside a git repo instead of the full filesystem path.
- `[git_status]` swaps Starship's defaults for compact glyphs: `⇡`/`⇣` for ahead/behind your upstream, `⇕` for diverged, and `+`/`!`/`?`/`$` for staged, modified, untracked, and stashed changes respectively.
- `[cmd_duration]` only shows up when a command takes 2 seconds or longer (`min_time = 2000`), so quick commands don't clutter the prompt with a `took 12ms` you don't care about.
- `[time]` and `right_format` push the clock and command duration to the right side of the terminal, keeping the left side focused on "where am I / what's my git status" instead of getting crowded with extra info.

### The result

With this in place, the left side of the prompt stays clean — directory, git branch/status glyphs, and a colored arrow — while the right side quietly shows how long your last command took (if it was slow) and the current time. None of these glyphs require a Nerd Font, so it works in a stock terminal without any extra font installation.

### References:

- [Starship — Guide](https://starship.rs/guide/)
- [Starship — Configuration](https://starship.rs/config/)
