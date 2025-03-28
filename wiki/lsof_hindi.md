# [डेबियन] Debian Almquist Shell (dash) lsof उपयोग: सक्रिय फ़ाइलों की सूची दिखाना

## Overview
lsof (List Open Files) एक उपयोगी कमांड है जो सिस्टम पर खोली गई फ़ाइलों की सूची प्रदान करता है। यह जानकारी उपयोगकर्ताओं को यह समझने में मदद करती है कि कौन सी प्रक्रियाएँ कौन सी फ़ाइलों के साथ काम कर रही हैं।

## Usage
lsof कमांड का मूल सिंटैक्स निम्नलिखित है:

```bash
lsof [options] [arguments]
```

## Common Options
lsof के कुछ सामान्य विकल्प निम्नलिखित हैं:
- `-a`: सभी निर्दिष्ट विकल्पों के लिए AND ऑपरेटर का उपयोग करें।
- `-c`: एक विशेष प्रक्रिया नाम के लिए फ़ाइलें दिखाएँ।
- `-u`: एक विशेष उपयोगकर्ता द्वारा खोली गई फ़ाइलें दिखाएँ।
- `-p`: एक विशेष प्रक्रिया आईडी (PID) के लिए फ़ाइलें दिखाएँ।
- `-i`: नेटवर्क कनेक्शनों की जानकारी दिखाएँ।

## Common Examples
यहाँ कुछ सामान्य उदाहरण दिए गए हैं:

1. सभी खोली गई फ़ाइलों की सूची प्राप्त करने के लिए:
   ```bash
   lsof
   ```

2. एक विशेष उपयोगकर्ता द्वारा खोली गई फ़ाइलें दिखाने के लिए:
   ```bash
   lsof -u username
   ```

3. एक विशेष प्रक्रिया द्वारा खोली गई फ़ाइलें देखने के लिए:
   ```bash
   lsof -p 1234
   ```

4. नेटवर्क कनेक्शनों की जानकारी प्राप्त करने के लिए:
   ```bash
   lsof -i
   ```

5. एक विशेष प्रक्रिया नाम के लिए फ़ाइलें दिखाने के लिए:
   ```bash
   lsof -c processname
   ```

## Tips
- lsof का उपयोग करते समय, सुनिश्चित करें कि आपके पास उचित अनुमति है, क्योंकि कुछ फ़ाइलें और प्रक्रियाएँ केवल विशेष उपयोगकर्ताओं के लिए उपलब्ध हो सकती हैं।
- lsof का आउटपुट बहुत बड़ा हो सकता है, इसलिए आप `grep` का उपयोग करके विशेष फ़ाइलों या प्रक्रियाओं को फ़िल्टर कर सकते हैं।
- lsof को नियमित रूप से उपयोग करना सिस्टम की निगरानी के लिए एक अच्छा अभ्यास है, खासकर जब आप यह देखना चाहते हैं कि कौन सी प्रक्रियाएँ सिस्टम संसाधनों का उपयोग कर रही हैं।