# lab06-debugging

# Setup 

Create a [Shadertoy account](https://www.shadertoy.com/). Either fork this shadertoy, or create a new shadertoy and copy the code from the [Debugging Puzzle](https://www.shadertoy.com/view/flGfRc).

Let's practice debugging! We have a broken shader. It should produce output that looks like this:
[Unbelievably beautiful shader](https://user-images.githubusercontent.com/1758825/200729570-8e10a37a-345d-4aff-8eff-6baf54a32a40.webm)

It don't do that. Correct THREE of the FIVE bugs that are messing up the output. You are STRONGLY ENCOURAGED to work with a partner and pair program to force you to talk about your debugging thought process out loud.

Extra credit if you can find all FIVE bugs.

# Solution

### Team members: Joanna Fisch, Rhuta Joshi

### Bugs:

|Line No.|Artifact/Issue that helped in identification|Correction|
|---|---|---|
|99|Compile time error, vec not found| Replaced vec with vec2|
|102|Made the image appear flat or with incorrect resolution|Passed remapped uv2 instead of uv to rayCast function|
|11|Everything appeared stretched along x axis|`iResolution.x/iResolution.x` replaced with `iResolution.x/iResolution.y`|
|76|Reflection not working, spheres looked flat shaded|Was reflecting eye about normal instead of dir about normal|
|18|Disappearing floor plane around edges of spheres|Very small value of max ray steps, updated from 64 to 256|

[Corrected shadertoy link](https://www.shadertoy.com/view/msBGRd)

# Submission
- Create a pull request to this repository
- In the README, include the names of both your team members
- In the README, create a link to your shader toy solution with the bugs corrected
- In the README, describe each bug you found and include a sentence about HOW you found it.
- Make sure all three of your shadertoys are set to UNLISTED or PUBLIC (so we can see them!)
