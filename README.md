<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Blog Writing Crew with CrewAI

**Project Link:** [View Project](http://nextwork.ai/projects/ai-crewai-blog-writing-crew)

**Author:** jaswant singh  
**GitHub:** [@JaswantOnGit](https://github.com/JaswantOnGit)

---

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_h6t9b3y7)

---

## Introducing Today's Project!

In this project, I am building a multi-agent AI system using CrewAI. I will create a team of specialized AI agents, a Researcher, a Writer, and an Editor that work together in a sequential workflow to research a topic, write a blog post, and edit it into a polished final version. I will configure the agents and tasks using YAML files, connect them through `crew.py`, and generate the final blog post as a Markdown file. As an optional extension, I can also add a fourth Social Media Manager agent to create Twitter/X thread and LinkedIn post summaries from the completed blog post.


### Key tools and concepts

In this project, I learned how to use CrewAI to build a multi-agent AI system where multiple AI agents collaborate to complete a task. I learned how to configure agents and tasks using agents.yaml and tasks.yaml, connect them in crew.py, and run them in a sequential workflow. I also learned how to use placeholders like {topic} to make the agents dynamic, manage project dependencies with uv, configure a Gemini API key to connect to a language model, and save the final output as a Markdown file. Finally, I learned how to extend the crew by adding a Social Media Manager agent and customize its behavior by modifying its backstory.

### Challenges and wins

It took me about 2–3 hours to complete this project. The most challenging part was understanding how the different CrewAI files work together, especially connecting the agents and tasks through crew.py and ensuring the method names matched the keys in the YAML files. Setting up the environment and configuring the Gemini API key also required careful attention, but once everything was connected correctly, the workflow ran smoothly.

### Personal reflection

Thank you for this project! I enjoyed learning how to build a multi-agent AI system using CrewAI. It helped me understand how AI agents can collaborate to complete tasks, and I gained hands-on experience with configuring agents, defining tasks, and connecting them into a working workflow. It was a valuable and practical learning experience.

---

## Installing Python and CrewAI

In this step, I am setting up my development environment so I can build and run my CrewAI project. I will install Python, the `uv` package manager, and the CrewAI CLI. I will also obtain a free Gemini API key to connect my AI agents to a large language model (LLM), which will power their reasoning and responses. These tools are required to create, manage, and run the multi-agent blog writing system successfully.


![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_v8bn4x1w)

### Understanding the uv package manager

`uv` is a fast Python package manager and virtual environment tool. CrewAI uses `uv` because it installs packages, manages dependencies, and creates virtual environments more quickly than traditional tools like `pip` and `virtualenv`. This makes setting up and managing CrewAI projects faster, simpler, and more efficient.


---

## Scaffolding the CrewAI Project

In this step, I am creating a new CrewAI project using the CrewAI CLI. The CLI generates the project's folder structure, configuration files, and starter code that I need to build my blog writing crew. I will also explore the project structure and configure my Gemini API key and model settings so my AI agents can connect to the language model and perform their tasks.


![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_v4nt8wf6)

### Key project files

Two key files in my project are .env and pyproject.toml. The .env file stores the Gemini API key and model configuration needed for the AI agents to work. The pyproject.toml file manages the project's dependencies and configuration.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_w2dc5nq8)

---

## Configuring AI Agents

In this step, I am defining the AI agents that will make up my blog writing crew. I will replace the default agents with three custom agents a Researcher, a Writer, and an Editor. I will configure each agent in agents.yaml by giving them a specific role, goal, and backstory so they know their responsibilities and can work together effectively to create a high quality blog post.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_j3x8n1v6)

### How agent configuration shapes AI behavior

The role, goal, and backstory fields define each agent's identity and responsibilities. The role describes what the agent is, the goal explains what the agent is trying to accomplish, and the backstory provides context that influences how the agent thinks and performs its tasks. The {topic} variable is used as a placeholder so the agents can dynamically adapt to the topic provided at runtime, allowing the same agent configuration to work for different blog topics without changing the YAML file.

---

## Defining the Task Pipeline

In this step, I am defining the tasks that each AI agent will perform in the tasks.yaml file. I will create three sequential tasks for the Researcher, Writer, and Editor, and assign each task to the appropriate agent. This is important because it gives each agent clear instructions, ensures they work together in the correct order, and allows the crew to produce a complete, polished blog post.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_p3n8v5w1)

### How the tasks chain together

The three tasks are connected in a sequential workflow. First, the Researcher gathers information and creates a research brief. Next, the Writer uses that research brief to write a complete blog post. Finally, the Editor reviews and improves the blog post by correcting grammar, improving clarity, and refining the overall flow. Only the editing task includes an output_file field because it produces the final polished version of the blog post, which is then saved as output/blog_post.md. The outputs of the earlier tasks are passed directly to the next task in memory, so they do not need to be saved to a file.

---

## Connecting YAML Configuration to Python

In this step, I am connecting my agents and tasks in Python so they can work as a complete CrewAI system. I will update crew.py to create the agents and tasks from the YAML configuration files and arrange them in a sequential workflow. I will also update main.py to provide the {topic} input when the crew runs. This turns the configuration files into a working blog writing crew.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_p3n8v2q6)

### Why method names must match YAML keys

The method names in crew.py need to match the keys in my YAML files because CrewAI uses those names to link the Python methods to the correct agent and task configurations. If the names do not match, CrewAI will not be able to find the corresponding definitions in agents.yaml or tasks.yaml, and the crew will not be created or run correctly.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_h8f4d6a2)

---

## Running the Blog Writing Crew

In this step, I am installing the required project dependencies and running my CrewAI project. I will make sure my Gemini language model is configured correctly so my AI agents can communicate with it. Then, I will run the crew and watch the Researcher, Writer, and Editor work together to generate a complete blog post. Finally, I will experiment with different topics to see how the crew adapts and produces different blog posts.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_p4n8v1q6)

### How the agents collaborated

The three agents collaborated by working in sequence. First, the Researcher gathered accurate facts, trends, and key insights about the topic and created a research brief. Next, the Writer used that research to write a well-structured and engaging blog post. Finally, the Editor reviewed the draft, corrected grammar and spelling, improved clarity and flow, and polished the content to produce a publication-ready blog post that was saved as a Markdown file.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_h6t9b3y7)

---

## Adding a Social Media Manager Agent

In this project extension, I am expanding my CrewAI system by adding a fourth AI agent called the Social Media Manager. This agent takes the final blog post created by the Researcher, Writer, and Editor and generates social media content, such as a Twitter/X thread and a LinkedIn post. I will also create a new task for this agent, run the updated crew, and experiment with the agent's backstory to change the tone and style of the social media posts.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_w3f8j1v6)

### Extending the crew with new agents and tasks

I updated three files: agents.yaml, tasks.yaml, and crew.py. In agents.yaml, I added a new social_media_manager agent with its role, goal, and backstory. In tasks.yaml, I added a social_media_task that generates a Twitter/X thread and a LinkedIn post from the final blog post. In crew.py, I added the new agent and task and included them in the crew's sequential workflow so the Social Media Manager runs after the Editor.

![Image](http://nextwork.ai/surprised_maroon_kind_alligator/uploads/ai-crewai-blog-writing-crew_t6c1g4q8)

### Social media output

My Social Media Manager agent produced a Twitter/X thread and a LinkedIn post based on the final blog post. Unlike the original blog post, which was longer and provided detailed information, the social media content was shorter, more concise, and optimized for each platform. The Twitter/X thread broke the key points into multiple engaging posts, while the LinkedIn post summarized the main ideas in a professional and reader-friendly format to encourage engagement.

### Experimenting with agent backstories

Changing the Social Media Manager's backstory changed the tone and style of the generated content. After updating the backstory to a more casual, Gen Z personality, the Twitter/X thread and LinkedIn post became more conversational, engaging, and energetic. The output included stronger hooks, a friendlier writing style, and emojis, making the social media posts feel more relatable and better suited for online audiences while still conveying the main points of the blog post.

---

---
