# [डेबियन] Debian Almquist Shell (dash) cd उपयोग: फ़ाइल सिस्टम में नेविगेट करें

## Overview
`cd` कमांड का उपयोग फ़ाइल सिस्टम में निर्देशिकाओं के बीच नेविगेट करने के लिए किया जाता है। यह आपको एक निर्देशिका से दूसरी निर्देशिका में जाने की अनुमति देता है।

## Usage
`cd` कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
cd [विकल्प] [आर्गुमेंट्स]
```

## Common Options
- `..` : पिछले निर्देशिका में जाने के लिए।
- `-` : पिछले निर्देशिका में वापस जाने के लिए।
- `~` : उपयोगकर्ता के होम निर्देशिका में जाने के लिए।

## Common Examples
1. **होम निर्देशिका में जाना:**
   ```bash
   cd ~
   ```

2. **पिछले निर्देशिका में जाना:**
   ```bash
   cd ..
   ```

3. **विशिष्ट निर्देशिका में जाना:**
   ```bash
   cd /path/to/directory
   ```

4. **पिछले निर्देशिका में वापस जाना:**
   ```bash
   cd -
   ```

## Tips
- हमेशा सुनिश्चित करें कि आप सही पथ का उपयोग कर रहे हैं, अन्यथा आपको "No such file or directory" त्रुटि मिल सकती है।
- `pwd` कमांड का उपयोग करके वर्तमान कार्यशील निर्देशिका की पुष्टि करें।
- यदि आप अक्सर किसी विशेष निर्देशिका में जाते हैं, तो आप इसे शॉर्टकट के रूप में सेट कर सकते हैं।