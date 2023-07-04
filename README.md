# Prettybox

*Prettybox* is a simple shell implementation to draw nice looking ascii
tables with auto sizing columns to the screen.

## Prerequisites

The `column` utillity as well as `sed` are needed for this script to work.

The implementation has been tested using *bash* as well as *zsh*.

## Installation

Options

* Copy and paste the code in your script
* Download it and chmod +x the script then save it somewhere on your PATH and source it
* If you have [basher](https://github.com/basherpm/basher) then `basher install Guang1234567/prettybox.sh`

## Usage

You may either source the `prettybox.sh` file or use it as an executable.
Both works just fine.
See [Installation](#installation) for install options.

Multiline table data is simply piped into `prettybox` for formating, while
the number of columns needs to be specified. Columns need to be delimited using
a `\t` (Tab) character.

Optionally a color may be specified as second argument to `prettybox`. This
color will be used to to color the header text. Available colors:

- blue
- green
- cyan
- red
- purple
- yellow
- gray
- light_blue
- light_green
- light_cyan
- light_red
- light_purple
- light_yellow
- light_gray


## Example

```bash
{
 printf 'PID\n';
 printf '%s\n' "foo bar";
 printf '%s\n' "blub blib blab bam boom";
} | prettybox green
```

```
┌──────────┬──────────────────────────┬─────────────────────────┐
│PID       │USER                      │APPNAME                  │
├──────────┼──────────────────────────┼─────────────────────────┤
│1         │john                      │foo bar                  │
│12345678  │someone_with_a_long_name  │blub blib blab bam boom  │
└──────────┴──────────────────────────┴─────────────────────────┘
```

**NOTE:** The spacing between lines is a result of Githubs formatting and should not occure in your terminal.
