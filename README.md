# Apple Valid Checker

A Windows command-line utility packaged for processing lists of email addresses and organizing check results into separate output files.

> **Note:** This repository contains a compiled executable. Its internal validation method, accuracy, and network behavior have not been independently verified. Output labels should not be treated as definitive proof that an Apple Account exists or that an email address is associated with one.

## Features

- **Batch input:** Reads email addresses from `mails.txt`.
- **Separated results:** Includes `result/live.txt` and `result/Dead.txt` for categorized output.
- **Windows executable:** Distributed as `Apple-VC.exe` for 64-bit Windows.
- **Simple folder structure:** Input, executable, and result files are organized in one directory.

## Requirements

- A 64-bit Windows environment.
- Permission to process the email addresses in your input list.
- Any additional runtime or network requirements imposed by the executable (not verified).

## Installation

1. Download and extract the ZIP archive.
2. Open the nested `apple valid checker` directory containing `Apple-VC.exe`.
3. Review the executable's provenance and scan it with your preferred security tools before running it.
4. Prepare `mails.txt` using email addresses you own or are authorized to test, with one address per line.

Example `mails.txt`:

```text
user1@example.com
user2@example.org
user3@example.net
```

## Usage

1. Place your authorized input list in `mails.txt`.
2. Run `Apple-VC.exe` on Windows.
3. Follow any prompts displayed by the program.
4. Inspect the contents of the `result/` folder afterward.

The exact on-screen workflow and meaning of the result categories have not been verified by a live execution.

## Project Structure

```text
apple valid checker/
└── apple valid checker/
    ├── Apple-VC.exe
    ├── mails.txt
    └── result/
        ├── live.txt
        └── Dead.txt
```

## Understanding Results

| File | Intended category |
| --- | --- |
| `result/live.txt` | Entries assigned to the `live` category by the program |
| `result/Dead.txt` | Entries assigned to the `Dead` category by the program |

These category names are inferred from the included filenames. They **do not by themselves establish** account existence, deliverability, account ownership, or service affiliation.

## Privacy & Responsible Use

Use this software only on email addresses you own or have explicit permission to test. Do not use it for unsolicited account discovery, user enumeration, spam, credential attacks, or unauthorized testing against third-party services. Follow applicable privacy rules and service terms.

**Before publishing the repository:** Remove real email addresses from `mails.txt`, clear any sensitive result files, and replace them with fictional examples. The supplied archive contains an email list that should not be uploaded publicly without review.

## Troubleshooting

- **Executable doesn't launch:** Check that you're using 64-bit Windows and review any security warnings. Do not disable antivirus protections to force execution.
- **No results generated:** Verify that `mails.txt` is present and correctly formatted. The program's error reporting has not been tested.
- **Unexpected output:** Treat the results as unverified until you understand the executable's underlying checks.

## Disclaimer

This project is not affiliated with, endorsed by, or sponsored by Apple Inc. Apple is a trademark of Apple Inc. The software is provided as-is; no guarantee is made regarding accuracy, availability, or suitability for any purpose.
