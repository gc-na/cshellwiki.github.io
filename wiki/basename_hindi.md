# [Linux] Bash basename उपयोग: फ़ाइल नाम निकालना

## Overview
`basename` एक Bash कमांड है जो दिए गए फ़ाइल पथ से फ़ाइल का नाम निकालता है। यह विशेष रूप से तब उपयोगी होता है जब आपको फ़ाइल के पूर्ण पथ से केवल नाम की आवश्यकता होती है।

## Usage
कमांड का मूल सिंटैक्स इस प्रकार है:
```
basename [options] [arguments]
```

## Common Options
- `-a`: एक से अधिक फ़ाइलों के लिए नाम निकालता है।
- `-s`: एक विशेष स्ट्रिंग को फ़ाइल नाम से हटाने के लिए उपयोग किया जाता है।

## Common Examples
1. एक साधारण फ़ाइल नाम निकालना:
   ```bash
   basename /home/user/document.txt
   ```
   **Output:** `document.txt`

2. एक विशेष स्ट्रिंग को हटाना:
   ```bash
   basename /home/user/document.txt .txt
   ```
   **Output:** `document`

3. एक से अधिक फ़ाइलों के लिए नाम निकालना:
   ```bash
   basename -a /home/user/file1.txt /home/user/file2.txt
   ```
   **Output:**
   ```
   file1.txt
   file2.txt
   ```

## Tips
- जब आप फ़ाइल नाम को एक विशेष एक्सटेंशन के बिना प्राप्त करना चाहते हैं, तो `-s` विकल्प का उपयोग करें।
- `basename` का उपयोग स्क्रिप्ट में फ़ाइल नामों को प्रोसेस करने के लिए करें, ताकि आप केवल आवश्यक जानकारी प्राप्त कर सकें।