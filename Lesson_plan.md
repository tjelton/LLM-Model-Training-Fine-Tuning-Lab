# Summary:

I am designing an AI literacy lab titled “Interactive Lab: Model Training and Finetuning”. This is part of an AI literacy course for tertiary students, where students come from diverse academic backgrounds. Importantly, students are not expected to know how to code. Still, they can be asked to run code and make minor changes, such as modifying parameter names as part of experimentation.
Main Directives:
Your objective is to make the lab that I explain in detail below. 
- I will NOT ask you to generate the entire lab at one time. Instead, I will instruct you to implement different components of the lab.
- If at any point you are unsure or think there is ambiguity about what to do next, ask clarifying questions.
- The lab must be generated as a static HTML site that can be deployed to GitHub Pages.
- Part of the lab will include coding exercises that will be placed on Google Colab. Create this in a separate Jupyter notebook file that I will later upload.

## Lab Content:

The site must use a modern multipage layout. While the site should look clean and stylistic, clarity is essential. The site will contain six pages, with the home page being the landing page. Most tasks will include group discussion questions or on-your-own-device questions. I want these to be formatted as clear call-outs, using consistent colours/icons for all tasks. The point of the group discussion questions is to get students to think deeply. The point of on-your-own-device questions is to get students to actively engage with the GPT2 model.

Between each task page, there should be buttons that take students home, or back to the previous or next task.

Whenever I ask you to work on the Jupyter notebook, all content should be in the same Jupyter notebook, yet clearly arranged.

## Home

On the home page, place a summary of the entire lab as a large paragraph. There should also be four rectangular buttons that take students to each of the four different tasks. When navigating between pages, use a slide-down animation to make the pages look fluid.
Task 1: Model Pre-Training

This first task acts to remind students of how models are initially trained. For this course, we want to expose students to only the fundamentals of how large language models (LLMs) are pre-trained. 

Step 1: Start with a brief paragraph introducing model pre-training and what will be covered in Task 1.

Step 2: Produce an interactive visualisation/diagram illustrating the important steps in model pre-training. This can include multiple slides that students click through. The important steps that must be included: tokenisation, embedding, attention, next-token prediction, loss calculation, backpropagation, scaling and iteration (indicating how the process is repeated billions of times to make the model better and better). Ensure that the explanations are accessible, and they should not go into complex detail.

Step 3: Write a short paragraph explaining how, after a model has been pre-trained, a user interacting with the model is using the same steps in the diagram in step 2, except we no longer need to do loss calculation, backpropagation, scaling and iteration. 

Group discussion questions:
1. Why is it that when a user is interacting with an LLM, the model no longer does the loss calculation, backpropagation, scaling and iteration steps? What would be the implications if these steps were still used?
2. How is LLM pre-training different from how humans learn language?
4. The model has learned statistical patterns about which tokens follow which. Does this mean the model 'understands' language? Why or why not?
3. What method do you think the model uses to predict the next token when a user interacts with an LLM?

## Task 2: Loading a GPT2 Model

In task 2, we are getting students to interact with a GPT2 model. 

Step 1: Write a brief paragraph about how GPT2 was released publicly online, and how we will be running it using the Keras library. In this, explain what Keras is.

Step 2: Explain that we will be using Google Colab to run this code. Explain briefly what Google Colab is, and then provide a link to the website (https://colab.research.google.com/). Explain that they will have to sign in with a Google account if they would like to do this themselves. If they would not, they can look on with another person in the group.

Step 3: Instruct students to watch the short video below (place a dummy YouTube video for now), where I will show students how to import the file we are working with today and how to use a free GPU. 

Step 4: Instruct students to run the code under the task 2 section. It is important that they run it while we go through task 3, as it can take some time to run.  

## Task 3: Ethical Considerations

In task 3, we get students to consider the different ethical issues in pre-training and fine-tuning models. In particular, students can choose between the following four case studies. There should be three buttons for each case study, which, when clicked, will open up some information about each case study. For now, just use dummy text for each case study, as I will expand each. Also, for each case study, embed a random YouTube video, as I will update this later. 

The titles of the four case studies are:
Environmental Impact
Slave labour
Copyright
(Fine-tuning) Toxic fine-tuning

For the fine-tuning example only, include a brief statement about how we have not talked about fine-tuning yet, but will be talking about it soon. For now, provide a very, very brief explanation of what fine-tuning is.

Group discussion questions:
1. As a group, explain the moral and ethical implications of your chosen case study. Who is harmed, who benefits, and is that trade-off justifiable?
2. Is self-regulation by AI companies sufficient, or is external oversight necessary?
3. Using an LLM of your choosing, what is some extra information you can find about this ethical topic that is not already included in the information above? Verify what the LLM says using a search engine.
4. What would it take for you to stop using an AI tool because of the ethical practices behind it?

## Task 4: Token Prediction

In task 4, we return to the Jupyter notebook from task 2. There should be a new section in the Google Colab file called task 4. In this section, we get students to use different sampling methods (especially greedy, k-beam, contrastive search and random sampler). 

Step 1: Write a brief paragraph about how, in task 1, when describing LLM generation, we did not really unpack how we choose the next token at inference time. Emphasise this by regenerating a simple version of the visualisation in task 2, with question marks at the point where tokens are generated. 

Step 2: Write a paragraph explaining how in this section, we will play around with different sampling methods (but do not go into the details of what these sampling methods do). Explain that these are different methods that are used to choose the next token from the list of probabilities. 

Step 3: In the Jupyter, prompt students to try different sampling methods, and to play around with different arguments. This is not a coding course, so make it very easy for students (be clear about what arguments they can modify).

Discussion Questions:
1. Create a table of prompt, greedy output, 5-beam output, contrastive search, and random sampler output. In your group, try 5 different prompts and compare the outputs using the different samplers. 
2. Which of the different sampling methods produced the most coherent and useful responses?
3. Hypothesise what each sampler does. After this, use your favourite LLM to briefly understand what these samplers do. 

## Task 5: Fine-tuning

In task 5, we get students to fine-tune the GPT model. 

Step 1: Write a brief paragraph explaining what fine-tuning is, and how it is different to pre-training. With this, create some sort of visualisation (it can have multiple slides) so that students can clearly see what is going on.

Step 2: Students will turn to their Jupyter notebook. In the notebook, there should be a section called Task 5. In this task, students will fine-tune the GPT2 notebook. There are two stages to this. The first stage is that students fine-tune the model using an inbuilt dataset (you can choose whatever dataset you like as long as it is appropriate). Students can then fine-tune GPT2 using that data. In the second stage, students can create their own dataset for fine-tuning. To facilitate this, create a Python list for them to place their sentences in. Explain how that works for the students (how the training sentences must have something in common for the LLM to pick up on the pattern), and how many sentences they should provide.

Discussion Questions:
1. Why would someone want to fine-tune an existing LLM such as GPT2?
2. Make a table where the columns are prompt, pre-trained GPT2, and fine-tuned GPT2. Write down 5 prompts and run them through each GPT2. Compare and discuss the outputs. What do we notice? Does fine-tuning look to have changed the behaviour of the LLM?
3. Repeat question 2, but using the fine-tuned model where you wrote the fine-tuning data.


