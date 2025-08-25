# Trace

The main startup file for trace.

This file can be launched directly from PyDM: `pydm trace/main.py`

## Arguments and Macros
Arguments and macros are parsed in this file. Valid arguments include:

- `-h`, `--help`:
    - Show the help message
- `-v`, `--version`:
    - Show the current version of trace
- `-i INPUT_FILE`, `--input_file INPUT_FILE`:
    - File path to import from
    - Alternatively can be passed as INPUT_FILE macro
    - Example:
        - `pydm trace/main.py -i trace/examples/FormulaExample.trc`
- `-p PV1 PV2 ...`, `--pvs PV1 PV2 ...`:
    - List of PVs to show on startup
    - Alternatively can be passed as PV or PVS macros
    - Takes string(s) representing the channels to connect to
    - Example:
        - `pydm trace/main.py -p FOO:BAR:CHANNEL SOME:OTHER:CHANNEL`
- `-m MACRO`, `--macro MACRO`:
    - Mimic PyDM macro replacements to use
    - Examples:
        - `pydm trace/main.py -m '{"PVS": ["FOO:BAR:CHANNEL", "SOME:OTHER:CHANNEL"]}'`
        - `pydm trace/main.py -m "INPUT_FILE = trace/examples/FormulaExample.trc"`

::: main
