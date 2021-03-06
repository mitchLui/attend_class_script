# Attendance Script

A python script that logs onto the University of Bristol Blackboard website and logs your attendance. Can be run manually or as a cron job.

## Requirements

Check `requirements.txt` for dependencies

Install dependencies:

```sh
pip3 install -r requirements.txt
```

You also need a `.env` file containing your credentials. See `.env.sample` for template.

## Available Units

| Class                               | Code          | Remarks    |
| ----------------------------------- | ------------- | ---------- |
| Computer Architecture               | "coms10015"   | N/A        |
| Imperative & Functional Programming | "coms10016"   | pin needed |
| OOP & Algorithms I                  | "coms10017"   | pin needed |


## Usage

Example

```sh
python3 take_attendance.py --unit <code> --pin <pin> --headless
```

options:

- `--unit` (compulsory ): unit number
- `--pin` (optional, defaults to None): class pin
- `--headless` (optional, defaults to False): whether to run in headless mode (Do not show browser while running)


Examples:

1. Attend Computer Architecture (coms10015)

```sh
python3 take_attendance.py --unit coms10015
```

2. Attend IFP

```sh
python3 take_attendance.py --unit coms10015 --pin 8768
```