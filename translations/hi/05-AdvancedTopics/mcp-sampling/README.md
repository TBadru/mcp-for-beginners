<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "3cb0da3badd51d73ab78ebade2827d98",
  "translation_date": "2025-06-12T22:09:41+00:00",
  "source_file": "05-AdvancedTopics/mcp-sampling/README.md",
  "language_code": "hi"
}
-->
## निश्चित सैम्पलिंग

ऐसे अनुप्रयोगों के लिए जहाँ लगातार एक जैसे परिणाम चाहिए, निश्चित सैम्पलिंग पुनरुत्पादन योग्य परिणाम सुनिश्चित करता है। यह एक निश्चित रैंडम सीड का उपयोग करके और तापमान को शून्य पर सेट करके ऐसा करता है।

आइए नीचे दिए गए उदाहरण को देखें जो विभिन्न प्रोग्रामिंग भाषाओं में निश्चित सैम्पलिंग को प्रदर्शित करता है।

## गतिशील सैम्पलिंग कॉन्फ़िगरेशन

स्मार्ट सैम्पलिंग प्रत्येक अनुरोध के संदर्भ और आवश्यकताओं के आधार पर पैरामीटर को समायोजित करता है। इसका मतलब है कि कार्य के प्रकार, उपयोगकर्ता की प्राथमिकताओं, या पिछले प्रदर्शन के आधार पर तापमान, top_p, और पेनल्टी जैसे पैरामीटर को गतिशील रूप से समायोजित करना।

आइए देखें कि विभिन्न प्रोग्रामिंग भाषाओं में गतिशील सैम्पलिंग को कैसे लागू किया जा सकता है।

## आगे क्या है

- [5.7 स्केलिंग](../mcp-scaling/README.md)

**अस्वीकरण**:  
यह दस्तावेज़ AI अनुवाद सेवा [Co-op Translator](https://github.com/Azure/co-op-translator) का उपयोग करके अनुवादित किया गया है। जबकि हम सटीकता के लिए प्रयासरत हैं, कृपया ध्यान दें कि स्वचालित अनुवाद में त्रुटियाँ या गलतियाँ हो सकती हैं। मूल दस्तावेज़ अपनी मूल भाषा में ही प्रामाणिक स्रोत माना जाना चाहिए। महत्वपूर्ण जानकारी के लिए पेशेवर मानव अनुवाद की सलाह दी जाती है। इस अनुवाद के उपयोग से उत्पन्न किसी भी गलतफहमी या गलत व्याख्या के लिए हम उत्तरदायी नहीं हैं।