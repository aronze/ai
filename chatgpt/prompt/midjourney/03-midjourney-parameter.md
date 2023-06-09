# Parameter List
Parameters are options added to a prompt that change how an image generates. Parameters can change an image's Aspect Ratios, switch between Midjourney Model Versions, change which Upscaler is used, and lots more.
Parameters are always added to the end of a prompt. You can add multiple parameters to each prompt.
## Basic Parameters
### Aspect Ratios
--aspect, or --ar Change the aspect ratio of a generation.
### Chaos
--chaos &lt;number 0–100&gt; Change how varied the results will be. Higher values produce more unusual and unexpected generations.
### No
--no Negative prompting, --no plants would try to remove plants from the image.
### Quality
--quality &lt;.25, .5, 1, or 2&gt;, or --q &lt;.25, .5, 1, or 2&gt; How much rendering quality time you want to spend. The default value is 1. Higher values cost more and lower values cost less.
### Repeat
--repeat &lt;1–40>, or --r &lt;1–40> Create multiple Jobs from a single prompt. --repeat is useful for quickly rerunning a job multiple times.
### Seed
--seed &lt;integer between 0–4294967295&gt; The Midjourney bot uses a seed number to create a field of visual noise, like television static, as a starting point to generate the initial image grids. Seed numbers are generated randomly for each image but can be specified with the --seed or --sameseed parameter. Using the same seed number and prompt will produce similar ending images.
### Stop
--stop <integer between 10–100&gt; Use the --stop parameter to finish a Job partway through the process. Stopping a Job at an earlier percentage can create blurrier, less detailed results.
### Style
--style &lt;4a, 4b, or 4c&gt; Switch between versions of the Midjourney Model Version 4
--style &lt;cute, expressive, or scenic> Switch between versions of the Niji Model Version 5
### Stylize
--stylize &lt;number&gt;, or --s &lt;number&gt; parameter influences how strongly Midjourney's default aesthetic style is applied to Jobs.
### tile
--tile parameter generates images that can be used as repeating tiles to create seamless patterns.
### Uplight
--uplight Use an alternative "light" upscaler when selecting the U buttons. The results are closer to the original grid image. The upscaled image is less detailed and smoother.
### Upbeta
--upbeta Use an alternative beta upscaler when selecting the U buttons. The results are closer to the original grid image. The upscaled image has significantly fewer added details.

## Model Version Parameters
Midjourney routinely releases new model versions to improve efficiency, coherency, and quality. Different models excel at different types of images.
### Niji
--niji An alternative model focused on anime style images.
### High Definition
--hd Use an early alternative Model that produces larger, less consistent images. This algorithm may be suitable for abstract and landscape images.
### Test
--test Use the Midjourney special test model.
### Testp
--testp Use the Midjourney special photography-focused test model.
### Version
--version <1, 2, 3, 4, or 5> or --v <1, 2, 3, 4, or 5> Use a different version of the Midjourney algorithm. The current algorithm (V4) is the default setting.

## Upscaler Parameters
Midjourney starts by generating a grid of low-resolution image options for each Job. You can use a Midjourney upscaler on any grid image to increase the size and add additional details. There are multiple upscale models available for upscaling an image.
### Uplight
--uplight Use an alternative "light" upscaler when selecting the U buttons. The results are closer to the original grid image. The upscaled image is less detailed and smoother.
### Upbeta
--upbeta Use an alternative beta upscaler when selecting the U buttons. The results are closer to the original grid image. The upscaled image has significantly fewer added details.

## Other Parameters
These parameters only work with specific earlier Midjourney Models
### Creative
--creative Modify the test and testp models to be more varied and creative.
### Image Weight
--iw Sets image prompt weight relative to text weight. The default value is --iw 0.25.
### Sameseed
--sameseed Seed values create a single large random noise field applied across all images in the initial grid. When --sameseed is specified, all images in the initial grid use the same starting noise and will produce very similar generated images.
### Video
--video Saves a progress video of the initial image grid being generated. Emoji react to the completed image grid with ✉️ to trigger the video being sent to your direct messages. --video does not work when upscaling an image.

## Compatibility
### Model Version & Parameter Compatability
|                       | Affects initial generation | Affects variations + remix | Ver. 5 | Ver. 4 | Ver. 3 | Test / | Testp | Niji | Niji 5 |
|-----------------------|----------------------------|----------------------------|--------|--------|--------|--------|-------|------|--------|
| Max Aspect Ratio      | ✓                          | ✓                          | any    | 1:2 or 2:1 | 5:2 or 2:5 | 3:2 or 2:3 | 1:2 or 2:1 | any    |
| Chaos                 | ✓                          |                            | ✓      | ✓      | ✓      | ✓      | ✓     | ✓    |        |
| Image Weight          | ✓                          |                            | .5–2 default=1 | any default=.25 |        |        | .5–2 default=1 |      |
| No                    | ✓                          | ✓                          | ✓      | ✓      | ✓      | ✓      | ✓     | ✓    | ✓      |
| Quality               | ✓                          |                            | ✓      | ✓      | ✓      |        | ✓     | ✓    |        |
| Repeat                | ✓                          |                            | ✓      | ✓      | ✓      | ✓      | ✓     | ✓    |        |
| Seed                  | ✓                          |                            | ✓      | ✓      | ✓      | ✓      | ✓     | ✓    |        |
| Sameseed              | ✓                          |                            |        |        | ✓      |        |       |      |        |
| Stop                  | ✓                          | ✓                          | ✓      | ✓      | ✓      | ✓      | ✓     | ✓    | ✓      |
| Style                 |                            |                            | 4a, and 4b |        |        |        | expressive, and cute |      |
| Stylize               | ✓                          |                            | 0–1000 default=100 | 0–1000 default=100 | 625–60000 default=2500 | 1250–5000 default=2500 |      | 0–1000 default=100 |      |
| Tile                  | ✓                          | ✓                          | ✓      |        | ✓      |        |       |      | ✓      |
| Video                 | ✓                          |                            |        |        | ✓      |        |       |      |        |
| Number of Grid Images | -                          | -                          | 4      | 4      | 4      | 2 (1 when aspect ratio≠1:1) | 4     |      |        |
