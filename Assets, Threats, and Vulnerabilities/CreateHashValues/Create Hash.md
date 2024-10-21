# Create Hash Value

## This lab consists of creating and evaluating the hash values for two files. You will use Linux commands to calculate the hash of two files and observe any differences in the hashes produced. Then, you'll determine if the files are the same, or different

### Scenario

In this scenario, we need to investigate whether two files are identical or different.

```bash
sha256sum file1.txt
sha256sum file2.txt

sha256sum file1.txt >> file1hash
sha256sum file2.txt >> file2hash

cmp file1hash file2hash
    Now, use the cmp command to compare the two files byte by byte. If a difference is found, the command reports the byte and line number where the first difference is found.
    Note: The output of the cmp command indicates that the hashes differ at the first character in the first line.
```
