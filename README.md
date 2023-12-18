# 🚀 Resources: Your Gateway to GenAI Mastery! 🌟

Thank you to everyone who participated in the [Advent of Gen AI](https://adventofgenai.com) Hackathon! It was an exciting 7-day event packed with innovative challenges, including creating a Stable Diffusion Comic Book Generator, working with LLMs and RAG, exploring Python code explainers, and more, all culminating in a 2-day development sprint.

Although the live hackathon has concluded, the adventure doesn't have to end. We're excited to announce that all the resources and challenges from the Advent of Gen AI are now available for you to explore offline. Whether you're looking to dive into the challenges at your own pace, expand your skills, or just satisfy your curiosity, our resources page is your gateway to continue learning and experimenting.

Dive into the world of generative AI and keep the spirit of innovation alive. Check out the [challenges](https://github.com/adventofgenai/challenges) and resources [https://github.com/adventofgenai/resources] and start your own Gen AI journey today!

Hello, AI Adventurers! Ready to navigate the exciting world of Generative AI with us? Here's everything you need to ace the [Advent of GenAI](https://adventofgenai.com) hackathon:


1. **GenAI GitHub Repository**
   - 🧭 Explore [rahulunair/genAI](https://github.com/rahulunair/genAI) for key insights on GenAI applications - Stable diffusion, LLM inference, finetuning and code generation with Intel GPUs. If you find the notebooks useful, consider leaving a star or spark a discussion with an issue!

2. **Intel Developer Cloud**
   
   - 🌐 Step into the [Intel Developer Cloud](https://cloud.intel.com) (IDC), register for free, and access Intel Xeons CPUs and GPUs. Discover a set of curated notebooks for Stable Diffusion, LLM inference and Finetuning on Intel under the 'Gen AI Essentials' section.
   - **Each notebook will give you access to:** 
      - Jupyter Notebook: Each participant will work within a Jupyter Notebook environment, optimized for Generative AI challenges. 
      - Disk Space: Upto 30 GB per user (Depending up on capacity). 
      - GPU: Intel GPU with 48 GB (Data Center Max 1100), tailored for AI applications. 
      - CPU: 4th Gen Intel Xeon. 

<div align=center>
<img width="600" alt="Screenshot 2023-12-02 at 12 40 16 PM" src="https://github.com/adventofgenai/resources/assets/786476/50f0cf09-1d2c-489c-a3d3-0fdb23214062"/>
</div>

<a name="prediction-guard"></a>
3. **Prediction Guard: Access a variety of privacy-conserving LLMs, validate outputs**
   - 🛡️ Explore [Prediction Guard Documentation](https://docs.predictionguard.com). Check out the "Getting Started" and "Using LLMs" pages to run your first text or chat completions with the Prediction Guard API or Python client.

      ```python
      import os
      import json
      import predictionguard as pg
   
      os.environ['PREDICTIONGUARD_TOKEN'] = "<your PG access token>"
   
      response = pg.Completion.create(
         model="Neural-Chat-7B",
         prompt="The advent of Gen AI hackathon is: "
      )
   
      print(json.dumps(
         response,
         sort_keys=True,
         indent=4,
         separators=(',', ': ')
      ))
      ```

   - 💪 Run through some of the examples in the [Using LLMs](https://docs.predictionguard.com/usingllms) section of the docs to learn more about basical prompting, prompt engineering, retrieval, chat, agents, etc.

4. **Magic of Prompt Engineering**:
   - Explore generative art techniques with [Stable Diffusion Prompt Book](https://openart.ai/promptbook), a resource we found online for diverse prompt ideas and creative exploration in AI art.

5. **Intel Extension for PyTorch (XPUs):**
   - 🔥 Check if XPU is ready:
     ```python
     import torch
     import intel_extension_for_pytorch
     print(f"torch.xpu.is_available()")
     ```
   - 📚 Dive deeper at [Intel XPU Tutorials](https://intel.github.io/intel-extension-for-pytorch/xpu/latest/tutorials/examples.html)

6. **BigDL & LLMs**
   - 🧙‍♂️ Experience LLM inference in 4-bit with [BigDL LLM Inference](https://github.com/intel-analytics/BigDL/blob/main/python/llm/example/GPU/HF-Transformers-AutoModels/Model/llama2/generate.py#L58)

7. **Detect Your AI Resources: The Discovery Commands**
   - 🔍 Uncover Intel GPUs and CPUs:
     ```bash
     echo "Intel GPUs:"
     xpu-smi  discovery 2> /dev/null
     echo "Intel Xeon CPU:"
     lscpu | grep "Model name"
     xpu-smi dump -m 18
     ```

8. **Python Package Installation: Effortlessly**
   - 📦 Streamline your installations:
     ```python
     import sys
     import site
     from pathlib import Path
     !echo "Installing..."
     !{sys.executable} -m pip cache purge > /dev/null
     !{sys.executable} -m pip install <python_package_name>
     !echo "Installation Complete."
      def get_python_version():
          return "python" + ".".join(map(str, sys.version_info[:2]))
      
      def set_local_bin_path():
          local_bin = str(Path.home() / ".local" / "bin") 
          local_site_packages = str(
              Path.home() / ".local" / "lib" / get_python_version() / "site-packages"
          )
          sys.path.append(local_bin)
          sys.path.insert(0, site.getusersitepackages())
          sys.path.insert(0, sys.path.pop(sys.path.index(local_site_packages)))
      
      set_local_bin_path()
     ```
   
9. **Craft Your Custom Conda Environment**
   - 🧪 Mix your perfect environment:
     ```bash
     conda clone pytorch-gpu <new_name>
     conda activate new_name
     conda install ipykernel
     ipykernel install <>
     conda install ...
     ```
     
10. **Vector Databases: Exploring with LanceDB**
    - 🗂️ Engage with [LanceDB VectorDB Recipes](https://github.com/lancedb/vectordb-recipes/blob/main/examples/multimodal_search/main.ipynb)

11.**Mastery in Retrieval Augmented Generation**
   - 🎓 Learn from [LangChain](https://python.langchain.com/docs/use_cases/question_answering/) and [Llama-index](https://docs.llamaindex.ai/en/stable/getting_started/concepts.html)
 
12. **Building LLM Applications: The Ultimate Guide**
    - 📘 Deep dive into [Llama-index Docs](https://docs.llamaindex.ai/en/stable/understanding/understanding.html)

# Contributing to GenAI 🤝

**Share Your Genius:**
- Got an innovative idea or an improvement? We're all ears! 🌟
- Fork the repository, push your changes, and open a pull request.
- Remember, every bit of contribution helps us sail further in the ocean of AI!

# Reporting Issues 🐛

**Spot Something Amiss?**
- Stumbled upon a bug or facing a challenge? Let us help! 🛠️
- Create an issue in the [GitHub repository](https://github.com/adventofgenai/genAI/issues) with a detailed description.
- Your keen eye helps us refine the experience for everyone!

