<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "904b689eda5a68cbafe656d53f9787c7",
  "translation_date": "2025-06-17T18:47:52+00:00",
  "source_file": "03-GettingStarted/03-llm-client/README.md",
  "language_code": "pa"
}
-->
ਵਧੀਆ, ਅਗਲੇ ਕਦਮ ਲਈ, ਆਓ ਸਰਵਰ ਉੱਤੇ ਕੈਪਬਿਲਿਟੀਜ਼ ਦੀ ਸੂਚੀ ਬਣਾਈਏ।

### -2 ਸਰਵਰ ਕੈਪਬਿਲਿਟੀਜ਼ ਦੀ ਸੂਚੀ ਬਣਾਉਣਾ

ਹੁਣ ਅਸੀਂ ਸਰਵਰ ਨਾਲ ਕਨੈਕਟ ਕਰਾਂਗੇ ਅਤੇ ਉਸ ਦੀਆਂ ਕੈਪਬਿਲਿਟੀਜ਼ ਮੰਗਾਂਗੇ:

### -3 ਸਰਵਰ ਕੈਪਬਿਲਿਟੀਜ਼ ਨੂੰ LLM ਟੂਲਜ਼ ਵਿੱਚ ਬਦਲਣਾ

ਸਰਵਰ ਕੈਪਬਿਲਿਟੀਜ਼ ਦੀ ਸੂਚੀ ਬਣਾਉਣ ਤੋਂ ਬਾਅਦ ਅਗਲਾ ਕਦਮ ਇਹ ਹੈ ਕਿ ਉਨ੍ਹਾਂ ਨੂੰ ਉਸ ਫਾਰਮੈਟ ਵਿੱਚ ਬਦਲਿਆ ਜਾਵੇ ਜੋ LLM ਸਮਝ ਸਕੇ। ਇਸ ਤਰ੍ਹਾਂ, ਅਸੀਂ ਇਹ ਕੈਪਬਿਲਿਟੀਜ਼ ਆਪਣੇ LLM ਲਈ ਟੂਲਜ਼ ਵਜੋਂ ਪ੍ਰਦਾਨ ਕਰ ਸਕਦੇ ਹਾਂ।

ਵਧੀਆ, ਹੁਣ ਅਸੀਂ ਕਿਸੇ ਵੀ ਯੂਜ਼ਰ ਦੀ ਬੇਨਤੀ ਨੂੰ ਸੰਭਾਲਣ ਲਈ ਤਿਆਰ ਨਹੀਂ ਹਾਂ, ਇਸ ਲਈ ਆਓ ਇਸ 'ਤੇ ਕੰਮ ਕਰੀਏ।

### -4 ਯੂਜ਼ਰ ਪ੍ਰੌਮਪਟ ਬੇਨਤੀ ਨੂੰ ਸੰਭਾਲਣਾ

ਕੋਡ ਦੇ ਇਸ ਹਿੱਸੇ ਵਿੱਚ ਅਸੀਂ ਯੂਜ਼ਰ ਦੀਆਂ ਬੇਨਤੀਆਂ ਨੂੰ ਸੰਭਾਲਾਂਗੇ।

ਵਧੀਆ, ਤੁਸੀਂ ਕਰ ਲਿਆ!

## ਅਸਾਈਨਮੈਂਟ

ਐਕਸਰਸਾਈਜ਼ ਵਿੱਚ ਦਿੱਤਾ ਕੋਡ ਲਵੋ ਅਤੇ ਕੁਝ ਹੋਰ ਟੂਲਜ਼ ਨਾਲ ਸਰਵਰ ਬਣਾਓ। ਫਿਰ ਐਕਸਰਸਾਈਜ਼ ਵਾਂਗ ਹੀ ਇੱਕ LLM ਵਾਲਾ ਕਲਾਇੰਟ ਬਣਾਓ ਅਤੇ ਵੱਖ-ਵੱਖ ਪ੍ਰੌਮਪਟਾਂ ਨਾਲ ਇਸ ਨੂੰ ਟੈਸਟ ਕਰੋ ਤਾਂ ਜੋ ਤੁਹਾਡੇ ਸਾਰੇ ਸਰਵਰ ਟੂਲਜ਼ ਡਾਇਨੈਮਿਕ ਤੌਰ 'ਤੇ ਕਾਲ ਹੋਣ। ਇਸ ਤਰ੍ਹਾਂ ਕਲਾਇੰਟ ਬਣਾਉਣ ਨਾਲ ਅੰਤਮ ਯੂਜ਼ਰ ਨੂੰ ਵਧੀਆ ਅਨੁਭਵ ਮਿਲਦਾ ਹੈ ਕਿਉਂਕਿ ਉਹ ਸਹੀ ਕਲਾਇੰਟ ਕਮਾਂਡਾਂ ਦੀ ਬਜਾਏ ਪ੍ਰੌਮਪਟਾਂ ਦੀ ਵਰਤੋਂ ਕਰ ਸਕਦਾ ਹੈ ਅਤੇ ਕਿਸੇ MCP ਸਰਵਰ ਦੇ ਕਾਲ ਹੋਣ ਤੋਂ ਬੇਖ਼ਬਰ ਰਹਿੰਦਾ ਹੈ।

## ਹੱਲ

[Solution](/03-GettingStarted/03-llm-client/solution/README.md)

## ਮੁੱਖ ਗੱਲਾਂ

- ਆਪਣੇ ਕਲਾਇੰਟ ਵਿੱਚ LLM ਸ਼ਾਮਿਲ ਕਰਨ ਨਾਲ ਯੂਜ਼ਰਾਂ ਲਈ MCP ਸਰਵਰਾਂ ਨਾਲ ਬਿਹਤਰ ਇੰਟਰੈਕਸ਼ਨ ਦਾ ਤਰੀਕਾ ਮਿਲਦਾ ਹੈ।
- ਤੁਹਾਨੂੰ MCP ਸਰਵਰ ਦੇ ਜਵਾਬ ਨੂੰ ਉਸ ਤਰੀਕੇ ਵਿੱਚ ਬਦਲਣਾ ਪੈਂਦਾ ਹੈ ਜੋ LLM ਸਮਝ ਸਕੇ।

## ਨਮੂਨੇ

- [Java ਕੈਲਕੁਲੇਟਰ](../samples/java/calculator/README.md)
- [.Net ਕੈਲਕੁਲੇਟਰ](../../../../03-GettingStarted/samples/csharp)
- [JavaScript ਕੈਲਕੁਲੇਟਰ](../samples/javascript/README.md)
- [TypeScript ਕੈਲਕੁਲੇਟਰ](../samples/typescript/README.md)
- [Python ਕੈਲਕੁਲੇਟਰ](../../../../03-GettingStarted/samples/python)

## ਵਾਧੂ ਸਾਧਨ

## ਅਗਲਾ ਕੀ ਹੈ

- ਅਗਲਾ: [Visual Studio Code ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਸਰਵਰ ਦਾ ਉਪਯੋਗ](/03-GettingStarted/04-vscode/README.md)

**ਡਿਸਕਲੇਮਰ**:  
ਇਹ ਦਸਤਾਵੇਜ਼ AI ਅਨੁਵਾਦ ਸੇਵਾ [Co-op Translator](https://github.com/Azure/co-op-translator) ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਅਨੁਵਾਦਿਤ ਕੀਤਾ ਗਿਆ ਹੈ। ਜਦੋਂ ਕਿ ਅਸੀਂ ਸਹੀਅਤ ਲਈ ਯਤਨ ਕਰਦੇ ਹਾਂ, ਕਿਰਪਾ ਕਰਕੇ ਧਿਆਨ ਰੱਖੋ ਕਿ ਆਟੋਮੇਟਿਕ ਅਨੁਵਾਦਾਂ ਵਿੱਚ ਗਲਤੀਆਂ ਜਾਂ ਅਣਸਹੀ ਤੱਥ ਹੋ ਸਕਦੇ ਹਨ। ਮੂਲ ਦਸਤਾਵੇਜ਼ ਆਪਣੀ ਮੂਲ ਭਾਸ਼ਾ ਵਿੱਚ ਪ੍ਰਮਾਣਿਕ ਸਰੋਤ ਮੰਨਿਆ ਜਾਣਾ ਚਾਹੀਦਾ ਹੈ। ਮਹੱਤਵਪੂਰਣ ਜਾਣਕਾਰੀ ਲਈ, ਪੇਸ਼ੇਵਰ ਮਨੁੱਖੀ ਅਨੁਵਾਦ ਦੀ ਸਿਫਾਰਸ਼ ਕੀਤੀ ਜਾਂਦੀ ਹੈ। ਅਸੀਂ ਇਸ ਅਨੁਵਾਦ ਦੀ ਵਰਤੋਂ ਤੋਂ ਉੱਪਜਣ ਵਾਲੀਆਂ ਕਿਸੇ ਵੀ ਗਲਤਫਹਮੀਆਂ ਜਾਂ ਭ੍ਰਮਾਂ ਲਈ ਜ਼ਿੰਮੇਵਾਰ ਨਹੀਂ ਹਾਂ।