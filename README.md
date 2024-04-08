# Geospatial Portfolio
## About
I am passionate about using remote sensing and spatial analysis to help build a more just and sustainable world. In 2023-2024 I completed a research project while studying with the University of New England, Australia, in which I used a Landsat NDVI time series to investigate the spatial and temporal dynamics of vegetation in the Blue Mountains National Park, NSW. Based on this experience, I am now pursuing a career in remote sensing and spatial analysis.

## Education
* Bachelor of Science from University of New England, NSW, Australia. Graduated 2003.
* Graduate Diploma in Education from University of New England, NSW, Australia. Graduated 2004.
* Graduate Diploma in Science (Applied Statistics) from University of New England, NSW, Australia. Completed; graduation pending.

## Projects
### Landsat NDVI Time Series 1988-2023, Blue Mountains National Park
This research project was a major component of the Graduate Diploma in Science (Applied Statistics) that I completed between June 2021 and February 2024. In this study a 3-monthly season-based time-series of the Normalised Difference Vegetation Index (NDVI) derived from [Digital Earth Australia’s](https://www.dea.ga.gov.au/) Landsat data cube was used to assess the spatial and temporal dynamics of native vegetation in a portion of the Blue Mountains National Park, New South Wales, Australia, for the 36-year period 1988-2023. The project demonstrated that higher variability in vegetation greeness was associated with areas and vegetation forms impacted more frequently by forest fires. The project required the use of several major Python data analysis and visualisation libraries including [Xarray](https://docs.xarray.dev/en/stable/index.html),  [Matplotlib](https://matplotlib.org/stable/index.html), [GeoPandas](https://geopandas.org/en/stable/), [Pandas](https://pandas.pydata.org/docs/index.html), [Rioxarray](https://corteva.github.io/rioxarray/stable/), and [Jupyter Lab](https://docs.jupyter.org/en/latest/). Analysis techniques included threshold classification, determining causes of time series non-stationarity, and cross-correlation of NDVI time series with climatic time series.

The following visualisations were produced using Python code as a part of the project.
**Key**
1. False-colour composite of the study area
2. Spatial plot and classification of the NDVI Coefficient of Variation
3. Time series plots of climatic variables

![Blue Mountains National Park Project](/img/BMNP.png)

### Beginner's Guide to Remote Sensing With Python
I could not have completed my Graduate Diploma research project without the assistance of the vibrant and supportive coding community that can be found on sites such as [Stack overflow](https://stackoverflow.com/), [Geographic Information Systems](https://gis.stackexchange.com/), and [Cross Validated](https://stats.stackexchange.com/). In an effort to give back some of what I learned along the way, I created a collection of short Jupyter Notebook tutorials called the [Beginner's Guide to Remote Sensing With Python](https://github.com/mjdear68/Beginners_Guide_to_Remote_Sensing_With_Python). The tutorials are intended to be at a level accessible to people with minimal to intermediate Python experience, with each covering a common remote sensing task. They are published on GitHub at [https://github.com/mjdear68/Beginners_Guide_to_Remote_Sensing_With_Python](https://github.com/mjdear68/Beginners_Guide_to_Remote_Sensing_With_Python). The code and image below are extracted from the [Further Techniques](https://github.com/mjdear68/Beginners_Guide_to_Remote_Sensing_With_Python/blob/master/Notebooks/Further_Techniques.ipynb) notebook.

```python
subplot_titles = ['Sep', 'Oct', 'Nov', 'Dec', 'Jan', 'Feb']

fg = NDVI.sel(time=slice('2019-09','2020-02')).plot(col='time', 
                                                    cmap='RdYlGn', 
                                                    figsize=(10,5), 
                                                    robust=True, 
                                                    col_wrap=3,
                                                    cbar_kwargs={'label':'NDVI'})

for i, ax in enumerate(fg.axs.flat):
        remove_labels_ticks(ax)
        ax.set_title(subplot_titles[i], fontsize=11)

fg.fig.suptitle('NDVI Spring Summer 2019-2020', y=1.05, fontsize=14);
```

![Beginner's Guide to Remote Sensing With Python Project](/img/BGtoRS.png)

<!-- 
### Sentinel 2 Change Detection, Greater Blue Mountains World Heritage Area 
-->
