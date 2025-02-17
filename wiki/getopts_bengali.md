# [লিনাক্স] Bash getopts ব্যবহার: অপশন প্যারামিটার পরিচালনা

## Overview
`getopts` কমান্ডটি Bash স্ক্রিপ্টে অপশন প্যারামিটার পরিচালনার জন্য ব্যবহৃত হয়। এটি স্ক্রিপ্টের মধ্যে কমান্ড লাইন আর্গুমেন্টগুলিকে সহজে পড়া এবং প্রক্রিয়া করার একটি উপায় প্রদান করে।

## Usage
`getopts` কমান্ডের মৌলিক সিনট্যাক্স হল:

```bash
getopts [options] [arguments]
```

## Common Options
- `-a`: অপশনগুলির জন্য একটি অ্যালিয়াস তৈরি করে।
- `-b`: অপশনগুলির জন্য একটি বেসিক ফর্ম্যাট নির্ধারণ করে।
- `-c`: অপশনগুলির সংখ্যা গণনা করে।

## Common Examples
### উদাহরণ 1: সাধারণ অপশন পড়া
```bash
#!/bin/bash
while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B with argument: $OPTARG"
      ;;
    c)
      echo "Option C with argument: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### উদাহরণ 2: একাধিক অপশন ব্যবহার
```bash
#!/bin/bash
while getopts "x:y:z:" opt; do
  case $opt in
    x)
      echo "X option with argument: $OPTARG"
      ;;
    y)
      echo "Y option with argument: $OPTARG"
      ;;
    z)
      echo "Z option with argument: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### উদাহরণ 3: ডিফল্ট অপশন
```bash
#!/bin/bash
while getopts "d:" opt; do
  case $opt in
    d)
      echo "Default option with argument: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

## Tips
- `getopts` ব্যবহার করার সময়, অপশনগুলির জন্য একটি স্পষ্ট এবং সংক্ষিপ্ত চিহ্ন ব্যবহার করুন।
- প্রতিটি অপশনের জন্য একটি `case` ব্লক তৈরি করুন যাতে অপশনগুলির প্রক্রিয়াকরণ সহজ হয়।
- স্ক্রিপ্টের শুরুতে `OPTIND=1` সেট করুন যাতে অপশনগুলি সঠিকভাবে পুনরায় পড়া যায়।