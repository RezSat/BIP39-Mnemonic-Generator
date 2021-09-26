# BIP39-Mnemonic-Generator

Credits to: Steven Hatzakis


A simplified python program for generating valid bip39 palindromic mnemonics, using an initial random entropy via the secrets module in Python for cryptographically secure entropy, then revealing the entropy in its various formats including hex, and as a bytearray before hashing to obtain the leading required number of bits from the hash digest in order to compute the checksum and complete the final word group. Palindromic mnemonics are also valid when the order of the words are reversed.

Formula: Initial entropy in bits /32 = checksum length in bits
initial entropy mod 11 = remaining bits + checksum = last word
Initial entropy + checksum = total bits /11 = total words.
