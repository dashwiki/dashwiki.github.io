# [डेबियन] Debian Almquist Shell (dash) strace उपयोग: सिस्टम कॉल्स का ट्रेसिंग

## Overview
`strace` एक शक्तिशाली उपकरण है जो प्रोग्राम के द्वारा किए गए सिस्टम कॉल्स और सिग्नल्स को ट्रेस करता है। यह डेवलपर्स और सिस्टम एडमिनिस्ट्रेटर्स के लिए बेहद उपयोगी है, क्योंकि यह किसी प्रोग्राम की कार्यप्रणाली को समझने में मदद करता है और समस्याओं का निदान करने में सहायक होता है।

## Usage
`strace` का मूल सिंटैक्स निम्नलिखित है:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: संक्षिप्त रिपोर्ट तैयार करता है, जिसमें प्रत्येक सिस्टम कॉल की संख्या और समय का सारांश होता है।
- `-e trace=<set>`: केवल विशेष सिस्टम कॉल्स को ट्रेस करने के लिए उपयोग किया जाता है। उदाहरण के लिए, `-e trace=open` केवल `open` कॉल्स को ट्रेस करेगा।
- `-o <file>`: आउटपुट को एक फ़ाइल में लिखता है, जिससे आप बाद में इसे देख सकते हैं।
- `-p <pid>`: पहले से चल रहे प्रोग्राम के PID को ट्रेस करने के लिए उपयोग किया जाता है।

## Common Examples
1. किसी प्रोग्राम को ट्रेस करना:
   ```bash
   strace ls
   ```

2. केवल `open` सिस्टम कॉल्स को ट्रेस करना:
   ```bash
   strace -e trace=open ls
   ```

3 आउटपुट को एक फ़ाइल में लिखना:
   ```bash
   strace -o output.txt ls
   ```

4 पहले से चल रहे प्रोग्राम को ट्रेस करना (मान लीजिए PID 1234 है):
   ```bash
   strace -p 1234
   ```

5 संक्षिप्त रिपोर्ट प्राप्त करना:
   ```bash
   strace -c ls
   ```

## Tips
- `strace` का उपयोग करते समय, ध्यान रखें कि यह प्रोग्राम के प्रदर्शन को प्रभावित कर सकता है, इसलिए इसे प्रोडक्शन वातावरण में सावधानी से उपयोग करें।
- आउटपुट को फ़ाइल में लिखने से आप बाद में इसे आसानी से विश्लेषण कर सकते हैं।
- यदि आप केवल कुछ विशेष सिस्टम कॉल्स में रुचि रखते हैं, तो `-e trace=<set>` विकल्प का उपयोग करें ताकि आउटपुट को संकीर्ण किया जा सके।