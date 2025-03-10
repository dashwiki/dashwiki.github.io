# [डेबियन] Debian Almquist Shell (dash) traceroute उपयोग: नेटवर्क पथ का पता लगाना

## Overview
`traceroute` कमांड नेटवर्क पर डेटा पैकेट्स के मार्ग का पता लगाने के लिए उपयोग किया जाता है। यह कमांड यह दर्शाता है कि एक पैकेट किसी विशेष गंतव्य तक पहुँचने के लिए किन-किन राउटर्स से गुजरता है।

## Usage
कमांड की मूल संरचना इस प्रकार है:
```bash
traceroute [options] [arguments]
```

## Common Options
- `-m <hops>`: अधिकतम हॉप्स की संख्या निर्धारित करता है।
- `-n`: रिवर्स DNS लुकअप को बायपास करता है और केवल आईपी पते दिखाता है।
- `-p <port>`: ट्रेसिंग के लिए उपयोग किए जाने वाले पोर्ट को निर्दिष्ट करता है।
- `-w <seconds>`: प्रत्येक हॉप के लिए टाइमआउट अवधि निर्धारित करता है।

## Common Examples
1. किसी गंतव्य की ट्रेसिंग करना:
   ```bash
   traceroute example.com
   ```

2. अधिकतम 15 हॉप्स के साथ ट्रेसिंग करना:
   ```bash
   traceroute -m 15 example.com
   ```

3. रिवर्स DNS लुकअप को बायपास करना:
   ```bash
   traceroute -n example.com
   ```

4. विशेष पोर्ट के साथ ट्रेसिंग करना:
   ```bash
   traceroute -p 80 example.com
   ```

## Tips
- `traceroute` का उपयोग करते समय, सुनिश्चित करें कि आपके नेटवर्क पर आवश्यक अनुमति हो।
- यदि आप धीमे नेटवर्क पर काम कर रहे हैं, तो `-w` विकल्प का उपयोग करके टाइमआउट अवधि बढ़ा सकते हैं।
- रिवर्स DNS लुकअप को बायपास करने के लिए `-n` विकल्प का उपयोग करें, जिससे परिणाम तेजी से प्राप्त हो सकें।