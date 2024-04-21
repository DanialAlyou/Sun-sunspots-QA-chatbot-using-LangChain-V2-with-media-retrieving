# Sun-sunspots-QA-chatbot-using-LangChain-V2 (with-media-retrieving)
A conversational retrieval chatbot to answer questions about sun and sunspots with media retrieving (as one of our graduation project features).

![General flow]([https://github.com/DanialAlyousef/Sun-sunspots-QA-chatbot-using-LangChain-V2/blob/8b725c8bc90cf4fa9a5badf835e2ed6eb1e978b8/images/general_chatbot_flow.png](https://github.com/DanialAlyou/Sun-sunspots-QA-chatbot-using-LangChain-V2-with-media-retrieving/blob/7c5a270ac3bc5d2b966de279a90751d1063ce753/images/general_chatbot_flow.png))



This project is an upgrade to our [last chatbot](https://github.com/DanialAlyou/Sun-sunspots-QA-chatbot-using-LangChain-V1/tree/main), it aims to create a chatbot to answer questions using preloaded documents about the sun and sunspots, the PDF files data was collected by [Tareq Alkhateb](https://www.linkedin.com/in/tareq-alkhateb-3359221a6/) from [Spaceweatherlive](https://Spaceweatherlive.com) and [britannica](https://www.google.com/url?q=https://www.britannica.com/&sa=U&ved=2ahUKEwjw8emZhNOEAxXwTKQEHWn5AhQQFnoECAEQAg&usg=AOvVaw1l8HbzB_akmwfBYUA36v8z), but with this upgrade we added media retrieving feature.

## What we did in this upgrade:
 - We reformatted the PDF files to make the documents retrieving easier and media retrieving possible.
 - Added a stage to check if the user input is a question related to our documents and if not, write a quick response for it, to reduce the LLM calls.
 - We used ConversationSummaryBufferMemory which keeps a buffer of recent interactions in memory, but when the interactions' number of tokens exceeds the "max_token_limit", it will summarize the chat history using the LLM.
 - built a media retriever.

## How do we retrieve media:
 - We reformatted the PDF files and split the chunks with "__________".
 - Some of these chunks have variables similar to the Python dictionary.
 - Each dictionary has data about the image/table ID and its description.
 - Using the "JsonOutputParser" we used the LLM for ID and description extraction from the documents.

## Notes:
 - If you are interested in trying out our chatbot or have any questions and need assistance, please don't hesitate to contact us. You can reach us via the following:
    -  Email: [Danial Alyousef](danial.emad.alyousef@gmail.com), [Mahmoud AboShuker](aboshukrmahmouf@gmail.com), [Tareq Alkhateb](Alkhateb31999@gmail.com).
    -  LinkedIn: [Danial Alyousef](https://www.linkedin.com/in/DanialAlyousef/), [Mahmoud AboShuker](https://www.linkedin.com/in/mahmoud-abo-shukr-485900270/), [Tareq Alkhateb](https://www.linkedin.com/in/tareq-alkhateb-3359221a6/)
 - if you are interested in our collected data don't hesitate to contact [Tareq Alkhateb](https://www.linkedin.com/in/tareq-alkhateb-3359221a6/).
 - Unfortunately, this version of our chatbot is customized to suit the upgrade, therefore, reusing it will not be a straightforward process like the [last version](https://github.com/DanialAlyousef/Sun-sunspots-QA-chatbot-using-LangChain-V1/tree/main), but we will be glad to help for educational and research purposes, you can reach us via E-mail or LinkedIn.
