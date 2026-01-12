# XOR Encryptor

## Description

A Python program that XOR encrypts shellcode.
It obfuscates the shellcode which may aid in passing security systems during pentesting.

## Features

- Simple XOR encryption/decryption for shellcode
- Accepts shellcode in both binary and text format
- Outputs in raw, python-array or C-array

## Requirements

- Python 3.x
- No external libraries required

## Installation

```bash
git clone https://github.com/Antonia634/xorencryptor.git
```

## Usage

```bash
python xorencryptor.py <input> <output> <key> [options]
```

### Arguments

| Argument | Description                               |
| -------- | ----------------------------------------- |
| `input`  | File containing shellcode to be encrypted |
| `output` | Output file for the encrypted shellcode   |
| `key`    | String key used for XOR encryption        |

| Option           | Description                                                         |
| ---------------- | ------------------------------------------------------------------- |
| `-f`, `--format` | Output format. Choices: `raw`, `python`, `c-array` (default: `raw`) |

## Examples

Encrypt shellcode and output raw binary:

```bash
python xorencryptor.py shellcode.bin xoredshellcode.xor mykey
```

Encrypt shellcode and output as a Python-array:

```bash
python xorencryptor.py shellcode.bin xoredshellcode.xor mykey -f python
```

Output:

```python
shellcode = [0x90, 0x90, 0xeb, 0xfe]
```

Encrypt shellcode and output as a C-array:

```bash
python xorencryptor.py shellcode.bin xoredshellcode.xor mykey -f python
```

Output:

```c
unsigned char xored_shellcode[] = {
    0x90, 0x90, 0xeb, 0xfe
};
```
