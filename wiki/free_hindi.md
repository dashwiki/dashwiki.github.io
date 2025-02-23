# [डेबियन] Debian Almquist Shell (dash) free मेमोरी की जानकारी: मेमोरी उपयोग की जानकारी दिखाना

## Overview
`free` कमांड सिस्टम की मेमोरी उपयोग की जानकारी प्रदान करता है। यह RAM और स्वैप मेमोरी के बारे में जानकारी देता है, जिससे उपयोगकर्ता यह समझ सकते हैं कि सिस्टम में कितनी मेमोरी उपलब्ध है और कितनी उपयोग में है।

## Usage
`free` कमांड का मूल स्वरूप इस प्रकार है:

```
free [options] [arguments]
```

## Common Options
- `-h`: मानव-पठनीय प्रारूप में आउटपुट दिखाता है (जैसे कि KB, MB, GB)।
- `-m`: मेमोरी की जानकारी मेगाबाइट्स में दिखाता है।
- `-g`: मेमोरी की जानकारी गीगाबाइट्स में दिखाता है।
- `-s <seconds>`: नियमित अंतराल पर मेमोरी की जानकारी दिखाने के लिए, जहां `<seconds>` वह समय है।

## Common Examples
1. मेमोरी की जानकारी को मानव-पठनीय प्रारूप में दिखाना:
   ```bash
   free -h
   ```

2. मेमोरी की जानकारी मेगाबाइट्स में दिखाना:
   ```bash
   free -m
   ```

3. हर 5 सेकंड में मेमोरी की जानकारी अपडेट करना:
   ```bash
   free -s 5
   ```

4. केवल स्वैप मेमोरी की जानकारी दिखाना:
   ```bash
   free | grep Swap
   ```

## Tips
- `free -h` का उपयोग करना सबसे अच्छा है क्योंकि यह जानकारी को आसानी से पढ़ने योग्य प्रारूप में प्रस्तुत करता है।
- नियमित रूप से मेमोरी उपयोग की निगरानी करने के लिए `-s` विकल्प का उपयोग करें, खासकर जब आप सर्वर पर काम कर रहे हों।
- आउटपुट को `grep` के साथ संयोजित करके विशेष जानकारी प्राप्त करें, जैसे कि केवल स्वैप मेमोरी।