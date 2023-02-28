# ❤️ a-better-shell-mommy
Simple [shell-mommy](https://github.com/sudofox/shell-mommy) script that works on zsh as well as bash.<br>

## Usage
Instead of running `mommy command`, this script just generates responses.
- Positive responses: `./shell-mommy.sh -p`
- Negative responses: `./shell-mommy.sh -n`

## Env vars
- `$MOMMYS_LITTLE` - what *you* will be called [default: `"girl"`]
- `$MOMMYS_ROLE` - what the *mommy* will be called [default: `"mommy"`]
- `$MOMMYS_PRONOUN` - what pronouns the *mommy* will use for itself [default: `"her"`]
- `$MOMMY_COLOR` - ansi escape code used at the start of the response for color [default: `'\e[38;5;217m'`]

## Example
**With env vars:**
```sh
"$MOMMYS_ROLE knows $MOMMYS_PRONOUN little $MOMMYS_LITTLE can do better~ ❤️"
```

**Defaults to:**
```sh
"mommy knows her little girl can do better~ ❤️"
```

## Add to .zshrc
**On successful commands:**
```sh
precmd() { [ $? -ne 1 ] && /path/to/shell-mommy -p }
```

**On failed commands:**
```sh
precmd() { [ $? -eq 0 ] && /path/to/shell-mommy -n }
```
