## 0:45
**User:** I'll call the message and append all of the user prompts into it.

## 0:49
**User:** While at it, I'll save the role type, in this case user, into the dictionary.

## 0:52
**User:** And then I can test it out. Hmm.

## 0:54
**User:** But the history doesn't show up.

## 0:56
**User:** Well, turns out I haven't printed out the historical messages... yet.

## 0:59
**User:** Loop through all the messages in the session state message variable and use the chat message component to display them.

## 1:04
**User:** And wait, did I save the app?

## 1:06
**User:** Of course not! I'd never make a mistake like that.

## 1:09
**User:** Let's just try that again...

## 1:10
**User:** and look at this!

## 1:12
**User:** Historical prompts that have been passed through.

## 1:14
**User:** Whoop de do, Nick. Where's the LLM at?

## 1:16
**User:** Well, let's do it.

## 1:17
**User:** I'm going to use the langchain interface to watsonx AI. Why?

## 1:20
**User:** Well, it uses state of art large language models, doesn't use your data to train, and it's built for business.

## 1:25
**User:** But that's just scraping the surface.

## 1:27
**User:** To do that, I'll create a credentials dictionary with an API key and use the ML service URL.

## 1:31
**User:** You can create an API key from the IBM Cloud IAM menu, URLs for different regions as shown on the screen right now.

## 1:36
**User:** Then the LLM! I'm using llam-2-70b-chat because I'm pretty fond of those furry buggers.

## 1:41
**User:** Pass through some decoding parameters and specify the project ID from watsonx.

## 1:45
**User:** Now then the prompt through to the LLM and boom.

## 1:48
**User:** Wait, it looks like it's running, but I need to show the LLM responses as well.

## 1:53
**User:** Easy enough with the streamlit chat message component.

## 1:55
**User:** Note the chat role for the LLM response is “assistant” rather than “user”. This helps to differentiate the responses.

## 1:59
**User:** I'll render the prompt as marked down and save the message to the session state as well.

## 2:04
**User:** That way, the history is displayed in the app. And... now it works.

## 2:08
**User:** Yeah, yeah, that's great. But where's the custom data come into play?

## 2:11
**User:** Enter phase three.

## 2:12
**User:** I’ll add in a load_pdf function and specify the name of the PDF file, then pass that to the langchain VectorstoreIndexCreator, and choose the embeddings function to use.

## 2:16
**User:** This basically chunks up the PDF and loads it into a vector database, Chromadb in this case.

## 2:20
**User:** Wrapping it in the st.cache_resource function means that streamlit doesn't need to reload it each time, which makes it a whole heap faster.

## 2:23
**User:** Anyway, I can then pass that index to the langchain RetrievalQA chain and swap out the base LLM the Q&A chain using chain.run.

## 2:37
**User:** And we can now chat with our PDF! In this case, a PDF to do with generative API.

## 2:42
**User:** Meta, I know.
