### Exercise 1
- Open *xy_16bit__microtubules.tif*
- Apply median filter with radius 1 and 3, respectively
- Estimate width of microtubules for non-filtered and filtered images using line profile,  **[Analyze > Plot Profile]**
- Repeat operation with a mean filter
- How dows the width of microtbules change


> ## Solution
>   - **[File > Open ...]** *xy_16bit__microtubules.tif*
>   - **[Image > Duplicate]** name *small_median*
>   - **[Image > Duplicate]** name *large_median*
>   - on *small_median* **[Process > Filters > Median]** radius 1
>   - on *large_median* **[Process > Filters > Median]** radius 3
>   - Draw a line with a line tool orthogonal to the MTs
>   - Measure line width using **[Analyze > Plot Profile]** or **[Ctrl-K]**
>    - Estimate width or in profile window **[Data>> > Add fit...]** and **[Fit function > Gaussian]** the parameter *d*  
>    is a proxy for the width (d = sigma). 
>   - Repeat for mean filter. 
{: .solution}

### Exercise 2
- Open *xy_8bit__nuclei_noisy_different_intensity.tif*
- Estimate radius of nuclei
- Apply median filter smaller than nucleus radius
- Apply median filter larger than nucleus radius
- Which radius can be use to
  - suppress noise
  - remove dark spot in one of the nuclei
  - remove both nuclei
- Compare median filter to mean filter of same radii
  - What are the advantages of a median filter?
  - What are the advantages of a mean filter?
- Apply a min filter of radius 1, what is happening?
- Apply a max filter of radius 1, what is happening?

> ## Solution
>   - **[File > Open ...]** *xy_8bit__nuclei_noisy_different_intensity.tif*
>   - Draw a line with a line along one of the nuclei and measure radius. **About 7 px**
>   -  Apply median filter smaller than nucleus radius. **noise is suppressed**
>   - Apply median filter larger than nucleus radius: **nuclei are shrinking**
>   - Which radius can be use to
>        - suppress noise **2**
>        - remove dark spot in one of the nuclei **1**
>        - remove both nuclei **20**
>    - Compare median filter to mean filter of same radii
>        - What are the advantages of a median filter? **edge preserving**
>        - What are the advantages of a mean filter? **small structure preserving**
>    - Apply a min filter of radius 1, can you describe what is happening? **nuclei shrink**
>    - Apply a max filter of radius 1, can you describe what is happening? **nuclei expand**
{: .solution}