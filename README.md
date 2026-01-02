# Feedback\_Gif\_Video\_Maker\_V1.0

A ComfyUI workflow designed for creating animated GIFs and videos using iterative feedback sampling techniques. This workflow leverages advanced image editing models to generate dynamic, evolving animations from text prompts or initial images.
    
## Examples

Here are some example outputs generated with this workflow:

![Elaphant Elegance](examples/Elaphant_Elagance.gif)

![Horseman of Many Forms](examples/horseman_of_many_Forms.gif)

![Pelicans Greed](examples/Pelicans_greed.gif)

![Zombie](examples/zombie.gif)


### Features

*   Feedback-based sampling for smooth morphing and evolving animations

*   Single image input, then uses qwen multiple angles lora to create variations. (prompts can be customised)

*   Ability to zoom/rotate/pan during animations

*   Uses RIFE frame interpolation to create smooth transitions between scenes
    
*   Support for GIF and video output
    

### Installation & Requirements

Required Custom NodesInstall these via ComfyUI Manager or manually:

*   Comfyui-FeedbackSampler: [https://github.com/QuorlenVerse/Comfyui-FeedbackSampler](https://github.com/QuorlenVerse/Comfyui-FeedbackSampler?referrer=grok.com) – Core feedback sampling functionality which adds ability to rotate and pan.
    (This is a forked version, creddit to orrigional creator https://github.com/pizurny/Comfyui-FeedbackSampler )
    
*   ComfyUI\_Fill-Nodes: [https://github.com/filliptm/ComfyUI\_Fill-Nodes](https://github.com/filliptm/ComfyUI_Fill-Nodes?referrer=grok.com) – Utility nodes for batching images, RIFE model loading.
    

Optional Custom Node (for GIF output)

*   ComfyUI-VideoHelperSuite: [https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite](https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite?referrer=grok.com)Required only if you want to save outputs as GIF format. If you don't need GIFs, you can mute or delete the Video Combine node in the workflow.

* Download links for all required models can be seen in the workflow notes (uses qwen image edit 2509 + lightning lora + Edit-2509-Multiple-angles lora + zimageturbo and all required text encoders and vae).

### How to Use

1.  Load the Feedback\_Gif\_Video\_Maker\_V1.0.json workflow in ComfyUI.
    
2.  Configure your prompt, seed, steps, rotation, zoom and feedback strength as desired.
    
3.  load your input image
    
4.  Queue the prompt and generate frames.
    
5.  Use the Video Combine node (if installed) to export as GIF or default save video for mp4.
    

Notes are included directly in the workflow JSON for more details.