# Streamlit AI Challenge

This repository was created for the Streamlit and Snowflake AI Challenge, which is taking place for 30 days in January 2026, led by Chanin Nantasenamat and Jessica Smith.

## 30 days AI Challenge Links


[Challenge Github](https://github.com/streamlit/30daysofai/).
[Challenge Details](https://30daysofai.streamlit.app/)


## 30 days AI Challenge Details


**Day 1**

Its all about connecting Streamlit app with Snowflake.

![Day 1](https://github.com/cooljay17/StreamlitAIChallenge/blob/main/Output/Day1.png)

**Day 2**

A streamlit app running an LLM directly inside Snowflake using the Cortex AI_COMPLETE function.

![Day 2](https://github.com/cooljay17/StreamlitAIChallenge/blob/main/Output/Day2.png)

**Day 3**

A streamlit app where user select a model, enter a prompt, and then stream the response back. Once that's done, display the AI's response in real-time, word by word, as it's being generated.

![Day 3](https://github.com/cooljay17/StreamlitAIChallenge/blob/main/Output/Day3.png)

**Day 4**

A streamlit app  that calls a Snowflake Cortex Large Language Model (LLM). An interface where a user can enter a prompt, send it to a powerful AI model (like Claude 3.5 Sonnet) running securely inside Snowflake, and get a response. Once that's done, display the AI's answer directly in the web app, along with how long the request took. Streamlit Cache is used to save the response.

![Day 4 First Submit](https://github.com/cooljay17/StreamlitAIChallenge/blob/main/Output/Day4_first.png)

![Day 4 Sccond Submit](https://github.com/cooljay17/StreamlitAIChallenge/blob/main/Output/Day4_second.png)


## Lessons Learned

**Day 1**

I always get confused when I come across the credentials I need to provide for a Snowflake account. At first, I tried entering the full URL — and bam! I got an error. Thankfully, after some hands-on learning, I was able to understand the difference between the account name, account locator, and organization. Once I entered the account locator, my Day 1 challenge worked perfectly.

**Day 2**

A reminder to self--
Special way to run streamlit app is
streamlit run <project folder>/StreamlitAIChallenge/Streamlitday2.py

AIComplete is the latest version of Complete and is stateless. Given model and prompt, it generates responses based on text or image or graphs etc. 

**Day 3**

Streaming eliminates long waiting times for a response. Rather than showing a blank screen or ‘Processing Response’, it’s much better to deliver instant output while the remaining response continues to load.

**Day 4**

Streamlit Cache has limitations. First time I gave a prompt and click submit, I received a response in 12 secondds. Next when I click Submit again, response was 0 seconds. So I thought of starting new session and give the same prompt . Alas the cache was not working. It seems there are limitations to Streamlit.

<ins> According to the documentation </ins>


> st.cache_data and st.cache_resource are not fully supported in Streamlit in Snowflake. Caching only works within a single session. Cached values can’t be carried over to other sessions and shared between different users of a Streamlit app.




