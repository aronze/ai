# Multi Prompts
It is possible to have the Midjourney Bot consider two or more separate concepts individually using :: as a separator. Separating prompts allows you to assign relative importance to parts of a prompt.
## Multi-Prompt Basics
Adding a double colon :: to a prompt indicates to the Midjourney Bot that it should consider each part of the prompt separately. In the example below, for the prompt hot dog all words are considered together, and the Midjourney Bot produces images of tasty hotdogs. If the prompt is separated into two parts, hot:: dog both concepts are considered separately, creating a picture of a dog that is warm.
There is no space between the double colons ::
Multi-prompts work with Model Versions 1, 2, 3, 4, '5, niji, and niji 5
Any parameters are still added to the very end of the prompt.
## Prompt Weights
When a double colon :: is used to separate a prompt into different parts, you can add a number immediately after the double colon to assign the relative importance to that part of the prompt.
In the example below, the prompt hot:: dog produced a dog that is hot. Changing the prompt to hot::2 dog makes the word hot twice as important as the word dog, producing an image of a dog that is very hot!
[Model Versions] 1, 2, 3 only accept whole numbers as weights
[Model Versions] 4 can accept decimal places for weights
Non-specified weights default to 1.
## Negative Prompt Weights
Negative weights can be added to prompts to remove unwanted elements.
The sum of all weights must be a positive number.
### Weights are normalized so:
tulips:: red::-.5 is the same as tulips::2 red::-1, tulips::200 red::-100, etc.
## The --no Parameter
The --no parameter is the same as weighing part of a multi prompt to "-.5" vibrant tulip fields:: red::-.5 is the same as vibrant tulip fields --no red.
