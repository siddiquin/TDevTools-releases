# TDevTools

**डेवलपरों के लिए मुफ़्त डेस्कटॉप टूलकिट: macOS, Windows और Linux पर JSON, XML, स्कीमा, API, एन्कोडिंग और प्रमाणपत्रों के लिए 47 टूल।**

[transposal.app](https://transposal.app) की ओर से

**भाषा चुनें:** [English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Türkçe](README.tr.md) · [日本語](README.ja.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md)

> **🔒 सब कुछ आपके कंप्यूटर पर चलता है। आपका डेटा कभी बाहर नहीं जाता।** TDevTools सारा काम आपके अपने कंप्यूटर पर करता है। आपकी JSON और XML फ़ाइलें, टोकन, कुंजियाँ और प्रमाणपत्र अपलोड नहीं होते और न ही एनालिटिक्स सेवाओं को भेजे जाते हैं। कोई खाता या ट्रैकिंग नहीं। ऐप इंटरनेट से केवल तभी जुड़ता है जब आप कहते हैं—जैसे URL लोड करना, अपने API को टेस्ट अनुरोध भेजना या सर्वर का प्रमाणपत्र प्राप्त करना। बाकी सभी टूल ऑफ़लाइन काम करते हैं।

## स्क्रीनशॉट

**JSON → JSON Schema:** नमूना डेटा से स्कीमा बनाएँ।

![JSON से JSON Schema](screenshots/json-to-schema.png)

**API टेस्टर:** अनुरोध भेजें और जवाब को ट्री, टेबल या टेक्स्ट में देखें।

![API टेस्टर](screenshots/api-tester.png)

**प्रमाणपत्र निरीक्षक:** प्रमाणपत्र श्रृंखला देखें और प्रमाणपत्रों तथा हस्ताक्षरों की जाँच करें।

![प्रमाणपत्र निरीक्षक](screenshots/certificate-inspector.png)

## डाउनलोड

नवीनतम संस्करण [Releases पेज](https://github.com/siddiquin/TDevTools-releases/releases/latest) से डाउनलोड करें।

| सिस्टम | डाउनलोड फ़ाइल |
| --- | --- |
| macOS, Apple Silicon (M1–M4) | `TDevTools-<version>-arm64.dmg` |
| macOS, Intel | `TDevTools-<version>-x64.dmg` |
| Windows 10/11, 64-बिट | `TDevTools-Setup-<version>-x64.exe` |
| Windows 10/11, ARM | `TDevTools-Setup-<version>-arm64.exe` |
| Windows, पोर्टेबल | `TDevTools-Portable-<version>.exe` |
| Linux, 64-बिट (x86_64) | `TDevTools-<version>-x86_64.AppImage` |
| Linux, ARM64 | `TDevTools-<version>-arm64.AppImage` |

**सिस्टम आवश्यकताएँ:** macOS 12 Monterey या नया; Windows 10/11 (64-बिट या ARM64); या कोई नया 64-बिट Linux वितरण (Ubuntu 20.04+, Debian 11+, Fedora 36+ या समान)। लगभग 300 MB खाली डिस्क स्थान चाहिए।

## इंस्टॉलेशन

### macOS

1. अपने Mac के लिए सही `.dmg` डाउनलोड करें, खोलें और लाइसेंस समझौते को स्वीकार करें।
2. **TDevTools** को **Applications** फ़ोल्डर में खींचें और डिस्क इमेज को बाहर निकालें।
3. पहली बार खोलते समय macOS चेतावनी दे सकता है कि ऐप को सत्यापित नहीं किया जा सकता, क्योंकि इस पर सशुल्क Apple Developer प्रमाणपत्र से हस्ताक्षर नहीं हैं। यह अपेक्षित है; अनुमति केवल एक बार देनी होगी।
   - **macOS 14 और उससे पहले:** Finder में TDevTools पर राइट-क्लिक करें, **Open** चुनें और फिर पुष्टि करें।
   - **macOS 15 और बाद के संस्करण:** ऐप खोलने का प्रयास करें और चेतावनी में **Done** चुनें। **System Settings → Privacy & Security** खोलें, TDevTools अवरोध संदेश के पास **Open Anyway** चुनें और पुष्टि करें।
4. यदि macOS कहता है कि «TDevTools क्षतिग्रस्त है», तो पहले सुनिश्चित करें कि आपने इसे आधिकारिक [Releases पेज](https://github.com/siddiquin/TDevTools-releases/releases/latest) से डाउनलोड किया है। फिर Terminal में `xattr -dr com.apple.quarantine /Applications/TDevTools.app` चलाएँ। इससे केवल इस ऐप का डाउनलोड क्वारंटीन चिह्न हटेगा।

### Windows

- **इंस्टॉलर:** `TDevTools-Setup-<version>-x64.exe` चलाएँ (ARM PC के लिए `arm64` फ़ाइल), लाइसेंस स्वीकार करें और **Install** चुनें। SmartScreen «Windows protected your PC» दिखाए तो **More info → Run anyway** चुनें। इंस्टॉलेशन केवल आपके खाते के लिए है; एडमिन अधिकार नहीं चाहिए।
- **पोर्टेबल संस्करण:** `TDevTools-Portable-<version>.exe` चलाएँ। SmartScreen आए तो **More info → Run anyway** चुनें।

### Linux (AppImage)

सही फ़ाइल डाउनलोड करें और **Properties → Permissions** में उसे चलाने की अनुमति दें या `chmod +x TDevTools-*.AppImage` चलाएँ। फिर डबल-क्लिक करें या Terminal से चलाएँ। यदि ऐप शुरू न हो, तो कुछ वितरणों में FUSE 2 चाहिए (Ubuntu/Debian: `sudo apt install libfuse2`; Ubuntu 24.04: `sudo apt install libfuse2t64`; Fedora: `sudo dnf install fuse-libs`)। ऐप मेनू में जोड़ने के लिए Gear Lever या AppImageLauncher इस्तेमाल कर सकते हैं।

## अपडेट और अनइंस्टॉल

नया संस्करण डाउनलोड करके उसी तरह इंस्टॉल करें; आपकी प्राथमिकताएँ बनी रहेंगी। macOS पर Applications में ऐप बदलें, Windows पर नया इंस्टॉलर चलाएँ और Linux पर AppImage फ़ाइल बदलें।

- **macOS:** TDevTools को Trash में डालें। प्राथमिकताएँ भी हटाने के लिए `~/Library/Application Support/TDevTools` हटाएँ।
- **Windows:** **Settings → Apps → Installed apps** से TDevTools हटाएँ। प्राथमिकताएँ हटाने के लिए `%APPDATA%\TDevTools` हटाएँ। पोर्टेबल संस्करण के लिए `.exe` हटाना पर्याप्त है।
- **Linux:** AppImage हटाएँ। प्राथमिकताएँ हटाने के लिए `~/.config/TDevTools` हटाएँ।

ऐप केवल थीम और भाषा जैसी प्राथमिकताएँ सहेजता है; आपके डेटा, पासवर्ड या कुंजियों की प्रतियाँ नहीं रखता।

## सुविधाएँ

- **फ़ॉर्मैट और सत्यापन:** JSON फ़ॉर्मैटर, वैलिडेटर, रिपेयर और विज़ुअल एडिटर; JSON, XML, CSV, Excel, YAML, TOON और JSONL रूपांतरण; Markdown, JSON/XML स्कीमा (XSD), और TypeScript टाइप जनरेशन।
- **सुरक्षा:** JWT डिकोड, सत्यापन और हस्ताक्षर; Base64/URL/SAML एन्कोडिंग; MD5, SHA-1 और SHA-256 हैश; सेल्फ-साइन्ड प्रमाणपत्र और mTLS किट बनाना; प्रमाणपत्र, सार्वजनिक कुंजी और JKS कीस्टोर जाँचना।
- **देखें और API:** JSON के ट्री, टेबल, ग्रिड, ग्राफ़ और Raw दृश्य; OpenAPI/Swagger ब्राउज़र, OAuth2 और mTLS वाला HTTP क्लाइंट, SOAP/WSDL व्यूअर, फ़ाइल व्यूअर और Markdown प्रीव्यू।
- **क्वेरी और रूपांतरण:** JSONPath टेस्टर, रेगेक्स के साथ खोज और बदलें, JavaScript/TypeScript/Python/C# में एक्सपोर्ट होने वाला JSON मैपर; वैकल्पिक क्लाउड सेवा Transposal Mapper।
- **तुलना:** JSON/XML संरचनात्मक अंतर और प्रति-पंक्ति त्रुटियों वाला JSON Schema सत्यापन।
- **पूरे ऐप में:** 8 भाषाएँ, 6 थीम, एक्सेंट रंग, घनत्व और ज़ूम, एक-क्लिक कॉपी, राइट-क्लिक मेनू, ड्रैग-एंड-ड्रॉप और स्टेटस बार में CPU/मेमोरी उपयोग।

## गोपनीयता और सुरक्षा

- सारा प्रोसेसिंग आपके कंप्यूटर पर होता है; चिपकाई या खोली गई कोई चीज़ अपलोड नहीं होती।
- कोई खाते, टेलीमेट्री या विज्ञापन नहीं।
- नेटवर्क से जुड़ना केवल आपके अनुरोध पर होता है, जैसे URL लोड करना, API टेस्ट करना या प्रमाणपत्र प्राप्त करना।
- पासवर्ड, टोकन और निजी कुंजियाँ ऐप खुला रहने तक केवल मेमोरी में रहती हैं; सिर्फ़ प्राथमिकताएँ सहेजी जाती हैं।
- अलग-थलग विंडो और सख्त Content Security Policy; HTML प्रीव्यू स्क्रिप्ट नहीं चलाते; किसी प्रोग्राम या स्क्रिप्ट को खोलने से पहले अनुमति माँगी जाती है; लॉगिन विवरण केवल आपके चुने सर्वर को भेजे जाते हैं।
- बिल्ट-इन उदाहरण सार्वजनिक डेमो सर्वर का उपयोग करते हैं और हर 2 मिनट में एक अनुरोध तक सीमित हैं। आपके अपने URL और फ़ाइलों पर कोई सीमा नहीं।

## अक्सर पूछे जाने वाले प्रश्न

**क्या TDevTools मुफ़्त है?** हाँ, यह डेवलपरों के लिए मुफ़्त है। [लाइसेंस समझौता](LICENSE.md) देखें।

**क्या यह ऑफ़लाइन काम करता है?** हाँ। केवल वे सुविधाएँ ऑफ़लाइन नहीं चलतीं जिन्हें आपके चुने सर्वर से बात करनी होती है, जैसे URL लोड करना, API/SOAP टेस्ट और प्रमाणपत्र श्रृंखला प्राप्त करना।

**क्या सोर्स कोड उपलब्ध है?** TDevTools क्लोज़्ड-सोर्स है। «TDevTools» विषय के साथ **<support@transposal.app>** पर ईमेल करके सोर्स कोड का अनुरोध करें।

**इंस्टॉल करते समय मेरा कंप्यूटर चेतावनी क्यों देता है?** ऐप पर सशुल्क Apple या Microsoft डेवलपर प्रमाणपत्र से हस्ताक्षर नहीं हैं, इसलिए पहली बार खोलने पर Gatekeeper और SmartScreen चेतावनी देते हैं। इंस्टॉलेशन निर्देशों का पालन करें और केवल आधिकारिक [Releases पेज](https://github.com/siddiquin/TDevTools-releases/releases/latest) से डाउनलोड करें।

## लाइसेंस और सहायता

- [अंतिम उपयोगकर्ता लाइसेंस समझौता](LICENSE.md): मुफ़्त उपयोग, बिना वारंटी। पूरा समझौता ऐप में **Help → License Agreement** के अंतर्गत 8 भाषाओं में उपलब्ध है।
- [तृतीय-पक्ष सूचनाएँ](THIRD_PARTY_NOTICES.md)
- सहायता: **<support@transposal.app>**
- वेबसाइट: [transposal.app](https://transposal.app)

© 2026 Transposal. सर्वाधिकार सुरक्षित।