---
title: Generative AI
permalink: /control-catalog/cybersecurity/ga/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls for the use of generative AI/LLMs within applications.

| Controls                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------- |
| [GA-1: Overseas-hosted GenAI API services](#ga-1-overseas-hosted-genai-api-services)                                            |
| [GA-2: Singapore-hosted GenAI API services](#ga-2-singapore-hosted-genai-api-services)                                          |
| [GA-3: Non-logging and non-training Agreement](#ga-3-non-logging-and-non-training-agreement)                                    |
| [GA-4: Data classification for self-hosted GenAI models](#ga-4-data-classification-for-self-hosted-genai-models)                |
| [GA-5: GenAI model formats and loaders](#ga-5-genai-model-formats-and-loaders)                                                  |
| [GA-6: File upload safeguards](#ga-6-file-upload-safeguards)                                                                    |
| [GA-7: Evaluation of GenAI accuracy, safety, and output quality ](#ga-7-evaluation-of-genai-accuracy-safety-and-output-quality) |
| [GA-8: Inform users about GenAI risks and limitations ](#ga-8-inform-users-about-genai-risks-and-limitations)                   |

## GA-1: Overseas-hosted GenAI API services

**Group:** Generative AI

### Control Statement

Use only up to RESTRICTED and SENSITIVE NORMAL data with GenAI API services served by models hosted overseas.

### Control Recommendations

Verify data classification with data owner before using the data with overseas GenAI API services. Ensure that these API services are accessed only via environments authorised for up to RESTRICTED and SENSITIVE NORMAL data. For SaaS tools with GenAI components, please refer to the [Central SaaS Portal](https://go.gov.sg/saasportal).

### Risk Statement

Primary data is at greater legal, privacy, and exfiltration risk when in transit and processed by GenAI API services hosted in other countries.

## GA-2: Singapore-hosted GenAI API services

**Group:** Generative AI

### Control Statement

Use only up to CONFIDENTIAL and SENSITIVE HIGH data with GenAI API services served by models hosted in Singapore.

### Control Recommendations

Verify data classification with data owner before using the data with Singapore-hosted GenAI API services. Ensure that these API services are accessed only via environments authorised for up to CONFIDENTIAL and SENSITIVE HIGH data. Check documentation for whether cross-region inferencing or overseas processing occurs under certain conditions.

### Risk Statement

Primary data carries legal, privacy, and exfiltration risk when in transit and processed by GenAI API services hosted in Singapore.

## GA-3: Non-logging and non-training Agreement

**Group:** Generative AI

### Control Statement

Obtain a legally-binding commitment from the GenAI API service provider that states that they do not log, store, nor retain input and output data, and that no input and output data are used for training GenAI models. Prompt caching (i.e. temporarily storing responses to frequently used prompts) is exempt from the above restriction on logging, storing, or retaining data, provided the cache time-to-live (TTL) is ≤ 24 hours.

### Control Recommendations

Ensure that the agreement covers all endpoints, parameters, outputs and models in use. Using GenAI API services provided by GCC 2.0 satisfies this control.

### Risk Statement

Without a legally binding agreement, the GenAI service provider can access primary data or logs through automated or manual checks that can expose classified data, or they may use the data for further training of their GenAI models.

## GA-4: Data classification for self-hosted GenAI models

**Group:** Generative AI

### Control Statement

Ensure that GenAI models are hosted in an environment that can host the highest data classification of government data contained in the system that the model is deployed in.

### Control Recommendations

Refer to relevant IM8 SSPs for controls that need to be met before hosting government data of a given data classification in that environment (e.g. in a Singapore-hosted GCC environment.)

### Risk Statement

Using GenAI models with data that is more classified than what its environment is permitted to hold may open up cybersecurity vulnerabilities for attackers to exfiltrate classified data.

## GA-5: GenAI model formats and loaders

**Group:** Generative AI

### Control Statement

Use approved formats (such as [ insert: param, ga-5_prm_1 ]) when using any open-weights GenAI models. Use approved loaders (such as [ insert: param, ga-5_prm_2 ]) to load open-weights GenAI models.

### Control Recommendations

Update GenAI model loaders frequently to hinder attacks.

### Risk Statement

Insecure model formats or loaders have been shown to be potential threat vectors that may allow for arbitrary code execution. Failure to use more secure formats or loaders may result in potential unauthorised access to the system.

### Parameters

| ID         | Type                        | Description                                |
| ---------- | --------------------------- | ------------------------------------------ |
| ga-5_prm_1 | list of model formats (str) | An example list of approved model formats. |
| ga-5_prm_2 | list of model loaders (str) | An example list of approved model loaders. |

## GA-6: File upload safeguards

**Group:** Generative AI

### Control Statement

Implement file upload safeguards if file uploads are enabled in the system.

### Control Recommendations

Examples of safeguards include but are not limited to: (1) Implementing Data Loss Protection (“DLP”) tools to monitor document uploads, (2) Disabling bulk or batch file uploads, such as by preventing users from selecting multiple files with a single action, or by requiring users to confirm the data security/sensitivity classification of each file individually before uploading, (3) Prompting users who upload excessively large files to review file contents and their collective data security/sensitivity classification.

### Risk Statement

Enabling file uploads in a generative AI application creates two key risks: (a) the possibility of sensitive data leaks if models are prompted to reveal information from uploaded files, and (b) the risk of exceeding permitted data classification levels — either by uploading multiple files without reassessing their collective classification, or by inadvertently uploading documents with a higher classification level due to human error.

## GA-7: Evaluation of GenAI accuracy, safety, and output quality

**Group:** Generative AI

### Control Statement

Test the accuracy, safety, and quality of the GenAI application&#39;s outputs, with clearly defined metrics, test scenarios, and criteria.

### Control Recommendations

Determine the adequate level of accuracy, safety, and output quality for your application. Develop tests to assess outputs on these dimensions. The complexity and structure of these tests should be tailored to the risk profile of your application. Document this approach and measure &amp; monitor results after relevant model, prompt, and dependency updates. 

### Risk Statement

Failure to evaluate models, prompts, and their dependencies (such as tool integrations and retrieval-augmented generation (RAG) systems) can result in low-quality outputs after updates or configuration changes.

## GA-8: Inform users about GenAI risks and limitations

**Group:** Generative AI

### Control Statement

Require users to explicitly acknowledge the risk of inaccurate or fabricated outputs (hallucinations), such as selecting a checkbox or clicking on an &#39;I Agree&#39; button before the application can be accessed.

### Control Recommendations

Include clauses about the risk of inaccurate / fabricated outputs in your Terms of Use. Indicate prominently in your application about the possibility of inaccurate or fabricated outputs. Ensure that educational materials, such as documentation, guides, playbooks, or workshops, highlight responsible use and best practices for users of the GenAI system.

### Risk Statement

Uninformed users may trust inaccurate model-generated outputs.