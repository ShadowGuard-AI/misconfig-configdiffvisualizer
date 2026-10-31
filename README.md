![Banner](banner.png)

# misconfig-ConfigDiffVisualizer
Generates a human-readable diff between two configuration files, highlighting added, removed, and modified settings. Uses the diff-match-patch library to create a visually clear comparison, especially useful for understanding configuration changes over time. - Focused on Check for misconfigurations in configuration files or infrastructure definitions

## Install
`git clone https://github.com/ShadowStrikeHQ/misconfig-configdiffvisualizer`
Then install the libraries the tool imports: `pip install -r requirements.txt`. The diff library, diff_match_patch, is imported when the program starts, so this step is required before the first run.

## Usage
`./misconfig-configdiffvisualizer [params]`

## Parameters
- `-h`: Show help message and exit
- `-o`: Path of the HTML page to write. It may not name either input file, under any spelling of the path, including a `./` spelling or a symlink to an input. Such a run refuses at exit 1 and both inputs are left unchanged.
- `-t`: No description provided
- `--ignore-whitespace`: Ignore whitespace differences.
- `--no-validation`: Skip validation of configuration files.

## Empty inputs
An empty input file is an error at exit 1, with a line naming the empty file. It is not rendered as a page holding the literal text null, and two empty files do not produce a completed diff page. This tool is a visualizer, not a gate: a finished page exits 0 whether or not the two files differ.

## License
Copyright (c) ShadowStrikeHQ
