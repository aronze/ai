# Aspect Ratios
The --aspect or --ar parameter changes the aspect ratio of the generated image. An aspect ratio is the width-to-height ratio of an image. It is typically expressed as two numbers separated by a colon, such as 7:4 or 4:3.
A square image has equal width and height, described as a 1:1 aspect ratio. The image could be 1000px × 1000px, or 1500px × 1500px, and the aspect ratio would still be 1:1. A computer screen might have a ratio of 16:10. The width is 1.6 times longer than the height. So the image could be 1600px × 1000px, 4000px × 2000px, 320px x 200px, etc.
The default aspect ratio is 1:1.
--aspect must use whole numbers. Use 139:100 instead of 1.39:1.
The aspect ratio impacts the shape and composition of a generated image.
Some aspect ratios may be slightly changed when upscaling.

# Chaos
The --chaos or --c parameter influences how varied the initial image grids are. High --chaos values will produce more unusual and unexpected results and compositions. Lower --chaos values have more reliable, repeatable results.
--chaos accepts values 0–100.
The default --chaos value is 0.
## The Influence of Chaos on Jobs
### Low --chaos values
Using a low --chaos value, or not specifying a value, will produce initial image grids that are slightly varied each time a Job is run.
prompt example: imagine/ prompt watermelon owl hybrid
### High --chaos Values
Using a higher --chaos value will produce initial image grids that are more varied and unexpected each time a Job is run.
prompt example: imagine/ prompt watermelon owl hybrid --c 50
### Very High --chaos Values
Using extremely high --chaos values will produce initial image grids that are varied and have unexpected compositions or artistic mediums each time a Job is run.
prompt example: imagine/ prompt watermelon owl hybrid --c 100

# Quality
The --quality or --q parameter changes how much time is spent generating an image. Higher-quality settings take longer to process and produce more details. Higher values also mean more GPU minutes are used per job. The quality setting does not impact resolution.
The default --quality value is 1. Higher values use more of your subscription's GPU minutes.
--quality accepts the values: .25, .5, and 1 for the default model. Larger values will be rounded down to 1.
--quality only influences the initial image generation.
--quality works with Model Versions 1, 2, 3, 4, 5 and niji.
## Quality Settings
Higher --quality settings aren't always better. Sometimes a lower --quality settings can produce better results—depending on the image you're trying to create. Lower --quality settings might be best for a gestural abstract look. Higher --quality values may improve the look of architectural images that benefit from many details. Choose the setting that best matches the kind of image you're hoping to create.
Prompt example: /imagine prompt woodcut birch forest --q .25

# Seeds
The Midjourney bot uses a seed number to create a field of visual noise, like television static, as a starting point to generate the initial image grids. Seed numbers are generated randomly for each image but can be specified with the --seed or --sameseed parameter. Using the same seed number and prompt will produce similar ending images.
--seed accepts whole numbers 0–4294967295.
--seed values only influence the initial image grid.
Identical --seed values using Model Versions 1, 2, 3, test, and testp will produce images with similar composition, color, and details.
Identical --seed values using Model Versions 4, 5, and niji will produce nearly identical images.
Seed numbers are not static and should not be relied upon between sessions.

# Stop
Use the --stop parameter to finish a Job partway through the process. Stopping a Job at an earlier percentage can create blurrier, less detailed results.
--stop accepts values: 10–100.
The default --stop value is 100.
--stop does not work while Upscaling.

# Stylize
This Midjourney Bot has been trained to produce images that favor artistic color, composition, and forms. The --stylize or --s parameter influences how strongly this training is applied. Low stylization values produce images that closely match the prompt but are less artistic. High stylization values create images that are very artistic but less connected to the prompt.
--stylize's default value is 100 and accepts integer values 0–1000 when using the default [V4 model].

# Tile
The --tile parameter generates images that can be used as repeating tiles to create seamless patterns for fabrics, wallpapers and textures.
--tile works with Model Versions 1, 2, 3 and 5.
--tile only generates a single tile. Use a pattern making tool like this Seamless Pattern Checker to see the tile repeat.
