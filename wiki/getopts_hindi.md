# [लिनक्स] Bash getopts उपयोग: विकल्पों को प्रबंधित करने का एक तरीका

## Overview
`getopts` एक Bash встроенная команда है जो स्क्रिप्ट में विकल्पों और तर्कों को प्रबंधित करने के लिए उपयोग की जाती है। यह विशेष रूप से उपयोगी है जब आप अपने स्क्रिप्ट को अधिक लचीला और उपयोगकर्ता के अनुकूल बनाना चाहते हैं।

## Usage
`getopts` का मूल सिंटैक्स निम्नलिखित है:

```bash
getopts [options] [arguments]
```

## Common Options
- `-a`: सभी विकल्पों को एक साथ प्राप्त करें।
- `-n`: स्क्रिप्ट का नाम निर्दिष्ट करें।
- `-o`: विकल्पों की सूची निर्दिष्ट करें।

## Common Examples

### उदाहरण 1: सरल विकल्प
```bash
#!/bin/bash

while getopts "ab:c" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B with argument: $OPTARG"
      ;;
    c)
      echo "Option C selected"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### उदाहरण 2: विकल्पों के साथ स्क्रिप्ट चलाना
```bash
./myscript.sh -a -b value -c
```

### उदाहरण 3: डिफ़ॉल्ट मान सेट करना
```bash
#!/bin/bash

flag_a=0
flag_b="default"

while getopts "a:b:" opt; do
  case $opt in
    a)
      flag_a=1
      ;;
    b)
      flag_b=$OPTARG
      ;;
  esac
done

echo "Flag A: $flag_a"
echo "Flag B: $flag_b"
```

## Tips
- हमेशा `getopts` के साथ एक `case` स्टेटमेंट का उपयोग करें ताकि आप विभिन्न विकल्पों को आसानी से प्रबंधित कर सकें।
- `OPTARG` का उपयोग करें जब आप किसी विकल्प के साथ एक तर्क प्राप्त कर रहे हों।
- स्क्रिप्ट के अंत में एक डिफ़ॉल्ट केस जोड़ें ताकि उपयोगकर्ता द्वारा गलत विकल्प दिए जाने पर एक स्पष्ट संदेश दिख सके।