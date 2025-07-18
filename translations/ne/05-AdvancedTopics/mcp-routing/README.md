<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "af40eab7bd6ebf7e607f982a5506a5b5",
  "translation_date": "2025-06-12T23:29:18+00:00",
  "source_file": "05-AdvancedTopics/mcp-routing/README.md",
  "language_code": "ne"
}
-->
## MCP मा स्याम्पलिङ र राउटिङ आर्किटेक्चर

स्याम्पलिङ मोडेल कन्टेक्स्ट प्रोटोकल (MCP) को एक महत्वपूर्ण भाग हो जसले अनुरोधहरूलाई प्रभावकारी रूपमा प्रक्रिया गर्ने र राउटिङ गर्ने अनुमति दिन्छ। यसले आउने अनुरोधहरूको विश्लेषण गरेर सबैभन्दा उपयुक्त मोडेल वा सेवा चयन गर्छ, जुन विभिन्न मापदण्डहरू जस्तै सामग्री प्रकार, प्रयोगकर्ता सन्दर्भ, र प्रणाली लोडमा आधारित हुन्छ।

स्याम्पलिङ र राउटिङलाई मिलाएर यस्तो बलियो आर्किटेक्चर तयार गर्न सकिन्छ जसले स्रोतहरूको सदुपयोगमा सुधार ल्याउँछ र उच्च उपलब्धता सुनिश्चित गर्छ। स्याम्पलिङ प्रक्रियाले अनुरोधहरूलाई वर्गीकरण गर्न प्रयोग गरिन्छ भने राउटिङले तिनीहरूलाई उपयुक्त मोडेल वा सेवामा पठाउँछ।

तलको चित्रले कसरी स्याम्पलिङ र राउटिङले मिलेर व्यापक MCP आर्किटेक्चरमा काम गर्छन् देखाउँछ:

```mermaid
flowchart TB
    Client([MCP Client])
    
    subgraph "Request Processing"
        Router{Request Router}
        Analyzer[Content Analyzer]
        Sampler[Sampling Configurator]
    end
    
    subgraph "Server Selection"
        LoadBalancer{Load Balancer}
        ModelSelector[Model Selector]
        ServerPool[(Server Pool)]
    end
    
    subgraph "Model Processing"
        ModelA[Specialized Model A]
        ModelB[Specialized Model B]
        ModelC[General Model]
    end
    
    subgraph "Tool Execution"
        ToolRouter{Tool Router}
        ToolRegistryA[(Primary Tools)]
        ToolRegistryB[(Regional Tools)]
    end
    
    Client -->|Request| Router
    Router -->|Analyze| Analyzer
    Analyzer -->|Configure| Sampler
    Router -->|Route Request| LoadBalancer
    LoadBalancer --> ServerPool
    ServerPool --> ModelSelector
    ModelSelector --> ModelA
    ModelSelector --> ModelB
    ModelSelector --> ModelC
    
    ModelA -->|Tool Calls| ToolRouter
    ModelB -->|Tool Calls| ToolRouter
    ModelC -->|Tool Calls| ToolRouter
    
    ToolRouter --> ToolRegistryA
    ToolRouter --> ToolRegistryB
    
    ToolRegistryA -->|Results| ModelA
    ToolRegistryA -->|Results| ModelB
    ToolRegistryA -->|Results| ModelC
    ToolRegistryB -->|Results| ModelA
    ToolRegistryB -->|Results| ModelB
    ToolRegistryB -->|Results| ModelC
    
    ModelA -->|Response| Client
    ModelB -->|Response| Client
    ModelC -->|Response| Client
    
    style Client fill:#d5e8f9,stroke:#333
    style Router fill:#f9d5e5,stroke:#333
    style LoadBalancer fill:#f9d5e5,stroke:#333
    style ToolRouter fill:#f9d5e5,stroke:#333
    style ModelA fill:#c2f0c2,stroke:#333
    style ModelB fill:#c2f0c2,stroke:#333
    style ModelC fill:#c2f0c2,stroke:#333
```

## अब के गर्ने

- [5.6 स्याम्पलिङ](../mcp-sampling/README.md)

**अस्वीकरण**:  
यो दस्तावेज AI अनुवाद सेवा [Co-op Translator](https://github.com/Azure/co-op-translator) प्रयोग गरी अनुवाद गरिएको हो। हामी शुद्धताका लागि प्रयासरत छौं, तर कृपया जान्नुहोस् कि स्वचालित अनुवादमा त्रुटि वा अशुद्धता हुनसक्छ। मूल दस्तावेज यसको मूल भाषामा अधिकारिक स्रोत मानिनुपर्छ। महत्वपूर्ण जानकारीका लागि व्यावसायिक मानवीय अनुवाद सिफारिस गरिन्छ। यस अनुवादको प्रयोगबाट उत्पन्न कुनै पनि गलत बुझाइ वा व्याख्याका लागि हामी जिम्मेवार छैनौं।