# AI Art Generator  

This project uses **Stable Diffusion** to generate **high-quality AI-generated artwork** from **text prompts**.  
It leverages **Hugging Face’s `diffusers` library** and **Stable Diffusion v1.5** to create unique, creative images.

---

##  What This Code Does
✅ **Installs Required Libraries** – `diffusers`, `transformers`, `torch`.  
✅ **Loads Stable Diffusion Model** – Uses `runwayml/stable-diffusion-v1-5`.  
✅ **Generates AI Art from Text** – Converts **text prompts into high-quality images**.  
✅ **Displays & Saves the AI-Generated Image** – Saves the generated image as **`ai_art.png`**.  

---

## Example Prompts
Try generating AI art with these prompts:
-  `"A fantasy castle floating in the sky"`
-  `"An astronaut riding a horse on Mars"`
-  `"A futuristic cyberpunk city with neon lights"`
-  `"A mystical forest with glowing mushrooms"`

---

##  Technologies Used
- **Python** – Core programming language.
- **Hugging Face Diffusers** – Stable Diffusion model integration.
- **Torch (PyTorch)** – Deep learning framework.
- **Transformers** – For pre-trained AI model support.

---

##  Installation and Setup

### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/username/AI-Art-Generator.git
cd AI-Art-Generator

 2️⃣ Install Dependencies

pip install diffusers transformers torch
3️⃣ Run the AI Art Generator
python generate_art.py
📜 Code Overview
from diffusers import StableDiffusionPipeline
import torch

# Load Stable Diffusion model
pipe = StableDiffusionPipeline.from_pretrained("runwayml/stable-diffusion-v1-5")
pipe.to("cuda")  # Use GPU for faster generation

# Generate AI Art from Text
def generate_image(prompt, steps=50, guidance=7.5):
    print(f"Generating: {prompt}")
    image = pipe(prompt, num_inference_steps=steps, guidance_scale=guidance).images[0]
    image.save("ai_art.png")
    return image

# Example prompt
prompt = "A futuristic cyberpunk city with neon lights"
image = generate_image(prompt)

# Display the image
image.show()
 Example Output
✅ Text Prompt: "A neon-lit futuristic cyberpunk city"
✅ Generated Image: (Replace with actual AI-generated image)

 Use Cases
AI Art Generation – Create artistic images from text.
 Concept Art & Design – Generate creative ideas for projects.
Creative AI Exploration – Experiment with AI-generated visuals.
