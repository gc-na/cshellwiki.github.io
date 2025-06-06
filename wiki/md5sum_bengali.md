# [লিনাক্স] C Shell (csh) md5sum ব্যবহার: ফাইলের এমডি5 হ্যাশ গণনা করা

## Overview
`md5sum` কমান্ডটি ফাইলের এমডি5 হ্যাশ মান গণনা করে। এটি সাধারণত ফাইলের অখণ্ডতা যাচাই করতে ব্যবহৃত হয়, যাতে নিশ্চিত হওয়া যায় যে ফাইলটি পরিবর্তিত হয়নি।

## Usage
`md5sum` কমান্ডের মৌলিক সিনট্যাক্স হল:

```csh
md5sum [options] [arguments]
```

## Common Options
- `-b`: বাইনারি ফাইলের জন্য এমডি5 হ্যাশ গণনা করে।
- `-c`: একটি ফাইল থেকে এমডি5 হ্যাশ যাচাই করে।
- `-t`: টেক্সট ফাইলের জন্য এমডি5 হ্যাশ গণনা করে।

## Common Examples
1. একটি ফাইলের এমডি5 হ্যাশ গণনা করা:
   ```csh
   md5sum myfile.txt
   ```

2. একাধিক ফাইলের এমডি5 হ্যাশ গণনা করা:
   ```csh
   md5sum file1.txt file2.txt file3.txt
   ```

3. একটি এমডি5 হ্যাশ ফাইল থেকে যাচাই করা:
   ```csh
   md5sum -c checksum.md5
   ```

4. একটি বাইনারি ফাইলের এমডি5 হ্যাশ গণনা করা:
   ```csh
   md5sum -b mybinaryfile.bin
   ```

## Tips
- এমডি5 হ্যাশ ব্যবহার করার সময় নিশ্চিত করুন যে ফাইলটি সঠিকভাবে সংরক্ষিত হয়েছে।
- এমডি5 হ্যাশের সাথে একটি টেক্সট ফাইল তৈরি করে তা যাচাই করার জন্য ব্যবহার করুন।
- ফাইলের অখণ্ডতা নিশ্চিত করতে নিয়মিত এমডি5 হ্যাশ পরীক্ষা করুন।