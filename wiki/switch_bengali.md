# [লিনাক্স] Bash switch ব্যবহার: একটি বিকল্প নির্বাচন করা

## Overview
Bash এর `switch` কমান্ড একটি শর্তাধীন বিবৃতি যা বিভিন্ন শর্তের ভিত্তিতে বিভিন্ন কোড ব্লক কার্যকর করার জন্য ব্যবহৃত হয়। এটি প্রোগ্রামিংয়ে একটি কার্যকরী উপায়, যা কোডের প্রবাহ নিয়ন্ত্রণ করতে সাহায্য করে।

## Usage
`switch` কমান্ডের মৌলিক সিনট্যাক্স হল:

```bash
switch [options] [arguments]
```

## Common Options
- `-e` : একটি নির্দিষ্ট শর্তের জন্য সমানতা পরীক্ষা করে।
- `-d` : ডিফল্ট শর্ত নির্ধারণ করে, যদি অন্য কোন শর্ত পূরণ না হয়।
- `-h` : সাহায্য তথ্য প্রদর্শন করে।

## Common Examples
নিচে কিছু সাধারণ উদাহরণ দেওয়া হল:

### উদাহরণ ১: মৌলিক switch ব্যবহার
```bash
switch $variable in
    option1)
        echo "Option 1 selected"
        ;;
    option2)
        echo "Option 2 selected"
        ;;
    *)
        echo "Default option"
        ;;
esac
```

### উদাহরণ ২: সংখ্যা পরীক্ষা
```bash
switch $number in
    1)
        echo "Number is one"
        ;;
    2)
        echo "Number is two"
        ;;
    *)
        echo "Number is something else"
        ;;
esac
```

### উদাহরণ ৩: স্ট্রিং পরীক্ষা
```bash
switch $color in
    "red")
        echo "Color is red"
        ;;
    "blue")
        echo "Color is blue"
        ;;
    *)
        echo "Color is unknown"
        ;;
esac
```

## Tips
- `switch` ব্যবহারের সময় নিশ্চিত করুন যে প্রতিটি শর্ত সঠিকভাবে লেখা হয়েছে।
- ডিফল্ট শর্ত ব্যবহার করা একটি ভাল অভ্যাস, যাতে অপ্রত্যাশিত ইনপুটের জন্য একটি প্রতিক্রিয়া থাকে।
- কোডের পাঠযোগ্যতা বাড়ানোর জন্য প্রতিটি শর্তের জন্য স্পষ্ট এবং সংক্ষিপ্ত বার্তা ব্যবহার করুন।