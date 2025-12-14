# Arctic Ice Maps Analysis
## Project Overview
This project analyzes long-term trends in Arctic sea ice concentration using satellite imagery data from the AMSR-E and AMSR2 missions (2002–2024). The goal was to process raw geospatial data to visualize seasonal ice variations and quantify the physical reduction of the ice cap over the last two decades.

## Key Features
* **Data Visualization:** Utilized Matplotlib to render color-coded maps of ice concentration from raw `.npy` files, handling orientation and coordinate mapping.
* **Time-Series Analysis:** Processed over 350 data files using `glob` and string manipulation to extract timestamps and construct a continuous timeline of ice coverage.
* **Quantitative Metrics:**
    * Calculated the number of pixels with significant ice concentration (>50%).
    * Computed the physical Total Ice-Covered Area (km²) by integrating concentration data with pixel-area data.
    * Analyzed "hard ice" extent (concentration >99%).
* **Trend Calculation:** Quantified specific ice loss by comparing minimum mean ice-covered areas from the 2004-2006 period against the 2022-2024 period.

## Tools Used
* **Python:**
* **NumPy:** Efficient array manipulation, handling `NaN` values (land), and statistical calculations (`np.nansum`, `np.nanmin`).
* **Matplotlib:** plotting 2D image data (`imshow`) and generating time-series graphs.
* **Glob:** File pattern matching for batch data processing.
