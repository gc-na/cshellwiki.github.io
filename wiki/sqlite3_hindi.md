# [लिनक्स] Bash sqlite3 उपयोग: SQLite डेटाबेस के साथ इंटरैक्ट करें

## Overview
sqlite3 एक कमांड-लाइन टूल है जिसका उपयोग SQLite डेटाबेस के साथ इंटरैक्ट करने के लिए किया जाता है। यह उपयोगकर्ताओं को डेटाबेस बनाने, संशोधित करने और क्वेरी करने की अनुमति देता है।

## Usage
sqlite3 कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: सहायता संदेश प्रदर्शित करता है।
- `-version`: sqlite3 का संस्करण दिखाता है।
- `-init <file>`: निर्दिष्ट फ़ाइल को प्रारंभ करने के लिए लोड करता है।
- `-batch`: बैच मोड में चलाता है, जो इंटरैक्टिव प्रॉम्प्ट को बंद कर देता है।

## Common Examples
1. एक नया डेटाबेस बनाना:
   ```bash
   sqlite3 mydatabase.db
   ```

2. एक तालिका बनाना:
   ```bash
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

3. डेटा जोड़ना:
   ```bash
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Alice');"
   ```

4. डेटा क्वेरी करना:
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

5. डेटाबेस से बाहर निकलना:
   ```bash
   sqlite3 mydatabase.db ".exit"
   ```

## Tips
- हमेशा अपने डेटाबेस का बैकअप लें, खासकर जब आप महत्वपूर्ण डेटा के साथ काम कर रहे हों।
- SQL क्वेरीज़ को एक फ़ाइल में लिखें और उसे sqlite3 के साथ इनिशियलाइज़ करें, इससे आपको बेहतर प्रबंधन में मदद मिलेगी।
- `-batch` विकल्प का उपयोग करें जब आप स्क्रिप्टिंग कर रहे हों, ताकि इंटरैक्टिव प्रॉम्प्ट से बचा जा सके।