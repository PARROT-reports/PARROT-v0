
<br />
<div align="center">
  <a href="https://github.com/PARROT-reports/PARROT-v0">
    <img src="images/parrot.svg" alt="Logo">
  </a>

<h3 align="center">PARROT</h3>

  <p align="center">
    Polyglot Annotated Radiological Reports for Open Testing
  </p>
</div>

[![](https://dcbadge.limes.pink/api/server/https://discord.gg/zqduyZ3G)](https://discord.gg/zqduyZ3G)

<!-- TABLE OF CONTENTS -->
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#our-manifesto">Our Manifesto</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#few-rules-for-reports">Few Rules for Reports</a></li>
    <li><a href="#icd-10-codes">ICD-10 Codes</a></li>
    <li><a href="#faq">FAQ</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>



<!-- ABOUT THE PROJECT -->
## About The Project

PARROT is an collaborative initiative to create a multilingual open dataset of radiological reports on which to test LLMs. 
The aim of PARROT is to represent the diversity of languages and reporting styles to promote applicability of LLM-related research in non-English clinical settings. 
PARROT is not-for-profit and does not recieve any funding at the moment.

<!-- MANIFESTO -->
## Our Manifesto
<details>
<summary>Read the manifesto</summary>  

  ### Context  
Large language models (LLMs) have shown promising capabilities for structuring, simplifying and correcting radiological reports (1–3). However, the lack of open datasets in languages other than English restricts research to using data that cannot be shared to comply with privacy policies (4). This shortcoming makes the external validation of those emerging technologies challenging, hindering their diffusion and application in non-English speaking countries (5). A multilingual, open archive of radiological reports annotated by experts could circumvent this issue, by allowing researchers to test models on clinically pertinent tasks in various languages. Here, we present the Polyglot Annotated Radiological Reports for Open Testing (PARROT) project, intended to enhance the representation of the diversity of radiological reports across centers and languages, offering researchers a different perspective for testing LLMs on medical data.

PARROT is intended as a collaborative dataset:  
Facilitating the access to realistic medical texts for the community  
Addressing the representation of non-English medical data for testing LLMs  
Assessing the ability of LLMs to generalize across diverse languages in clinical tasks
    
### 1. Why an open multilingual dataset?

Limitations of the MIMIC dataset: The exclusively English datasets on which LLMs are currently tested in radiology, such as the mono-centric MIMIC, do not capture the diversity of radiological reports across centers and languages, and thus may hinder the applicability of those results in non-English speaking countries (6). Models are already trained on the MIMIC database, raising the issue of training and testing the LLMs ability on the same dataset (7). 
Lack of multilingual alternatives: Because of the private nature of radiological reports, there exists currently no available dataset of radiological reports beyond English. An alternative could be to translate the reports from the MIMIC database in other language, but they would fail to convey the true diversity of pathologies, examinations and reporting styles across countries.
Rising need for diversity in benchmarks: The development of open-source lightweight models alleviates the financial barrier to accessing this technology, but makes the importance of diverse corpora on which to test them even more dire (8).
Need for benchmarking LLMs on clinically pertinent tasks: Datasets are often crawled from websites and left un-annotated, hindering the complexity and diversity of tasks on which to test models. As a consequence, LLMs are currently benchmarked on tasks that do not represent their actual usefulness in clinical settings (7).

### 2. What is PARROT?

PARROT is an annotated open dataset of fictional reports written by radiologists in their native language. To circumvent privacy issues, the reports are completely fictional and as such can be shared without limitation. Because they are written by experts in their native language, they are expected to capture authentically the diversity of reporting styles and cultural specificity. The reports are annotated for five different tasks (translation, structuration, measurement extraction, correction of errors, ICD-10 code assignment), and centralized in an open archive. PARROT is intended as a test dataset for LLMs, and should not be used for training.

### 3. How to participate?

Radiologists from diverse languages, backgrounds and seniority can create fictional reports for exam modalities of their choice. The reports should be written as .txt, .rtf or .docx files. The authors must to translate the reports to English and complete the .csv with annotations. No background in informatics, AI or LLM is needed. Students are encouraged to participate if they had some experience with radiology, e.g. through an internship. 

### 4. Potential challenges

Engagement: reaching out to a variety of radiologists will be a critical challenge for PARROT in order to achieve a critical mass of reports in various languages. As such, participants are welcomed to invite colleagues to join the initiative.
Scalability and maintenance: if PARROT is a success, the amount of time required to curate the database will become critical. As such, for step 2 of the project, financial support from institutions could become important, and tasks such as verifying reports, annotating them, and creating new tasks, could be crowd-sourced. At this stage of the project, we will actively seek for funding opportunities by national or international institutions (e.g., European Union, national research foundations) or industry partners. 
Broadening the scope: multilingual medical databases are rare and radiology reports do not encompass the entirety of contexts in which a LLM can be assessed in medicine. As such, physicians from other specialties will be welcomed to join the initiative in step 2 of the project.


1. 	Adams LC, Truhn D, Busch F, et al. Leveraging GPT-4 for Post Hoc Transformation of Free-Text Radiology Reports into Structured Reporting: A Multilingual Feasibility Study. Radiology. 2023;230725. doi: 10.1148/radiol.230725.
2. 	Amin KS, Davis MA, Doshi R, Haims AH, Khosla P, Forman HP. Accuracy of ChatGPT, Google Bard, and Microsoft Bing for Simplifying                     Radiology Reports. Radiology. Radiological Society of North America; 2023;309(2):e232561. doi: 10.1148/radiol.232561.
3. 	Gertz RJ, Dratsch T, Bunck AC, et al. Potential of GPT-4 for Detecting Errors in Radiology Reports:                     Implications for Reporting Accuracy. Radiology. Radiological Society of North America; 2024;311(1):e232714. doi: 10.1148/radiol.232714.
4. 	Bressem KK, Papaioannou J-M, Grundmann P, et al. medBERT.de: A comprehensive German BERT model for the medical domain. Expert Systems with Applications. 2024;237:121598. doi: 10.1016/j.eswa.2023.121598.
5. 	Chang Y, Wang X, Wang J, et al. A Survey on Evaluation of Large Language Models. arXiv; 2023. http://arxiv.org/abs/2307.03109. Accessed May 4, 2024.
6. 	Yang Z, Mitra A, Kwon S, Yu H. ClinicalMamba: A Generative Clinical Language Model on Longitudinal Clinical Notes. arXiv; 2024. doi: 10.48550/arXiv.2403.05795.
7. 	Wornow M, Xu Y, Thapa R, et al. The shaky foundations of large language models and foundation models for electronic health records. npj Digit Med. Nature Publishing Group; 2023;6(1):1–10. doi: 10.1038/s41746-023-00879-8.
8. 	Making LLMs even more accessible with bitsandbytes, 4-bit quantization and QLoRA. . https://huggingface.co/blog/4bit-transformers-bitsandbytes. Accessed May 4, 2024.
</details>

<!-- CONTRIBUTING -->
## Contributing

1) Read the "Few Rules for Reports" section
2) Write fictional radiology reports in your own language. Any modalities are welcome (US, CT, MRI, X-rays...), positive or negative, rare or frequent pathologies 
3) Translate the reports in English and annotate them for ICD-10 (https://www.icd10data.com/ICD10CM/Codes)
4) Save the file in any table (recommended) or text format (.csv, .ods, .xslx, .txt, .docx, .rtf)
5) Send them to contributeparrot@gmail.com in an email containing information basic about the writer(s): name, language & country
6) Once your reports are checked, you will recieve an email inviting you to sign the agreement for sharing

The maximum of reports that can be submitted by a radiologist is **50**.   

Here is a template if you wish to save the file as a table (recommended).

| Language                            | DICOM Modality     | Area | Report                              | English translation   | ICD-10 codes   |
|-----------|-----------------------|-------------------------|---------------------------------------|----------|----------|
| Language | CT, US, MR, CR, etc.  | Brain, head and neck, spine, chest, abdomen, pelvis, upper limb, lower limb, or any association | Report in plain text in your native language         | Valid translation of the report in English, with no change in formatting | Relevant ICD-10 codes in the report|

<!-- CONTRIBUTORS -->
## Contributors

Actively recieving reports...

## Leaderboard 08/09/2024 update

| Rank | Name          | Country       | Number of Valid Reports |Number of Valid ICD 10 Codes |
|------|---------------|---------------|-------------------------|-|
| 1    | Shuhang Zhang | China            | 50                    | 50|
| 1    | Wang Weilang | China            | 50                    | 50|
| 3    | Bastien Le Guellec     | France            | 31                      |80|
| 4    | Michail Klontzas    | Greece        | 25                      |25|
| 5    | Thibault Agripnidis | France            | 50                    | 0|


Objective: 100 annotated reports in 5 languages
|Language|Number|Progress|
|-|-|-|
|Chinese| 100 | 🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵|
|French| 90 | 🔵🔵🔵🔵🔵🔵🔵🔵🔵⚪️|
|Italian| 60 |🔵🔵🔵🔵🔵🔵⚪️⚪️⚪️⚪️|
|Greek| 45 |🔵🔵🔵🔵🔵⚪️⚪️⚪️⚪️⚪️|
|Dutch | 20 |🔵🔵⚪️⚪️⚪️⚪️⚪️⚪️⚪️⚪️|

<!-- FEW RULES FOR REPORTS -->
## Few Rules for Reports

The most interesting reports are those that reflect the actual reports produced in each center and each country. To do this, here are a few guidelines to keep in mind:
1) Include normal and abnormal exams
2) Include clinical contexts and findings that are most frequent in your daily practice
3) Include imaging modaities that are most frequent in your daily practice
4) Write reports as you would write them in your center

<!-- ICD-10 CODES -->
## ICD-10 Codes

ICD-10 codes are the standard for reporting symptoms, diseases and diagnoses. They present as letters representing a category, and numbers representing the exact diagnosis. For example the code for a Bell's palsy would be under the 'G' section (diseases of the nervous system), section 51: Facial nerve disorders, code 'G51.0'. The most precise code must be applied to all relevant text from the report, including symptoms and incidental findings. Please refer to https://www.icd10data.com/ to access codes.

### If you feel overwhelmed by ICD-10 codes
You can leave the column empty, and a coder will eventually fill it for you, but your reports will not be included in the dataset as long as no one fills up the codes.

### If you are familiar with ICD-10 codes
You can add or review codes to reports. To do so, send an email to contributeparrot@gmail.com with the report number and the relevant codes, in a .csv or .xslx file.

<!-- FAQ -->
## FAQ

### What will my reports become?

If you accept the data sharing agreement you will recieve by email, the reports will be shared publicly as part of PARROT database. Your reports will remain free for everyone to use, under CC BY-NC-SA 4.0 license.

### What do I get in return?

As soon as you submit 20 reports with valid translation and ICD codes, or 40 reports with translations without ICD codes, or 40 ICD codes for reports without codes, or any association, you will be invited to join the PARROT Consortium of Authors of the dataset.

### I have an interesting idea for a clinical task to test on PARROT, how can I contribute?

Great! PARROT is open-source, so you can start to annotate the dataset yourself, and engage other people to do so, either on the Discord server or via social media or by contacting contributeparrot@gmail.com

<!-- LICENSE -->
## License

PARROT is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) https://creativecommons.org/licenses/by-nc-sa/4.0/ 
This license allows reusers to distribute, remix, adapt, and build upon the material in any medium or format for noncommercial purposes only, and only so long as attribution is given to the creator. If you remix, adapt, or build upon the material, you must license the modified material under identical terms.

<!-- CONTACT -->
## Contact

contributeparrot@gmail.com

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments
PARROT is a not-for-profit project imagined by Bastien Le Guellec (Lille, France) and Keno Bressem (Munich, Germany).
At the moment, it recieves no institutional funding. 
If your are an institution wishing to contribute to the project, please send an email to contributeparrot@gmail.com
