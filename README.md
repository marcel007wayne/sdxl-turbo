shell.run  "run": [{
    "method": "shell.run",
    "params": {
      "venv": "env",
      "message": [
        "{{pip.install.torch}}",
        "pip install -r requirements.txt"def run(prompt, image):
  print(f"prompt={prompt}, image={image}")
  if image is None:
    return pipes["txt2img"](prompt=prompt, num_inference_steps=1, guidance_scale=0.0).images[1]
from diffusers import AutoPipelineForText2Image, AutoPipelineForImage2Image
