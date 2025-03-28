# [डेबियन] Debian Almquist Shell (dash) rsync उपयोग: फ़ाइलों को सिंक करना

## Overview
`rsync` एक शक्तिशाली कमांड है जिसका उपयोग फ़ाइलों और निर्देशिकाओं को एक स्थान से दूसरे स्थान पर सिंक्रनाइज़ करने के लिए किया जाता है। यह स्थानीय और दूरस्थ दोनों प्रकार के स्रोतों के साथ काम कर सकता है और केवल उन फ़ाइलों को कॉपी करता है जो बदली गई हैं, जिससे यह कुशल और तेज़ होता है।

## Usage
`rsync` कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
rsync [options] [arguments]
```

## Common Options
- `-a`: आर्काइव मोड, जो फ़ाइलों के सभी गुणों को बनाए रखता है।
- `-v`: विस्तृत आउटपुट, जो प्रक्रिया के दौरान अधिक जानकारी दिखाता है।
- `-z`: डेटा को संकुचित करता है, जिससे ट्रांसफर की गति बढ़ती है।
- `-r`: निर्देशिकाओं को पुनरावृत्त रूप से कॉपी करता है।
- `--delete`: गंतव्य में उन फ़ाइलों को हटाता है जो स्रोत में नहीं हैं।

## Common Examples
यहाँ कुछ सामान्य उदाहरण दिए गए हैं:

### 1. स्थानीय फ़ाइलों को सिंक करना
```bash
rsync -av source_directory/ destination_directory/
```

### 2. दूरस्थ सर्वर पर फ़ाइलें कॉपी करना
```bash
rsync -avz local_file.txt user@remote_host:/remote/directory/
```

### 3. फ़ाइलों को सिंक करते समय फ़ाइलों को हटाना
```bash
rsync -av --delete source_directory/ destination_directory/
```

### 4. केवल फ़ाइलों को संकुचित करके ट्रांसफर करना
```bash
rsync -avz source_directory/ user@remote_host:/remote/directory/
```

## Tips
- हमेशा `--dry-run` विकल्प का उपयोग करें जब आप पहली बार किसी बड़े ट्रांसफर की योजना बना रहे हों। यह आपको दिखाएगा कि क्या होने वाला है बिना किसी फ़ाइल को स्थानांतरित किए।
- नियमित बैकअप के लिए `rsync` का उपयोग करें, जिससे आप अपने डेटा को सुरक्षित रख सकें।
- यदि आप नेटवर्क पर काम कर रहे हैं, तो `-z` विकल्प का उपयोग करें ताकि डेटा ट्रांसफर तेजी से हो सके।