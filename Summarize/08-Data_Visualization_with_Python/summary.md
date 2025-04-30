# Data Visualization with Python

## Introduction
Data visualization is the graphical representation of information and data using visual elements like charts, graphs, and maps. It provides an accessible way to understand trends, outliers, and patterns in data. Python offers several powerful libraries for creating compelling visualizations.

## Key Visualization Libraries

### Matplotlib
- **Foundation library** for most Python visualization
- Created in 2003 as a MATLAB-like plotting interface
- Provides low-level control over plot elements
- Core functions:
  - `plt.plot()` - Line plots
  - `plt.scatter()` - Scatter plots
  - `plt.bar()` - Bar charts
  - `plt.hist()` - Histograms
  - `plt.boxplot()` - Box plots
  - `plt.subplot()` - Multiple plots in one figure

### Seaborn
- Built **on top of Matplotlib** with a higher-level interface
- Specializes in **statistical visualizations**
- Features attractive default styles and color palettes
- Key functions:
  - `sns.histplot()` - Enhanced histograms
  - `sns.boxplot()` - Box plots with categorical variables
  - `sns.scatterplot()` - Scatter plots with additional dimensions
  - `sns.heatmap()` - Visualization of matrix data
  - `sns.pairplot()` - Pairwise relationships in dataset
  - `sns.FacetGrid()` - Subplot grid for conditional plotting

### Plotly
- **Interactive visualizations** that work well in web contexts
- Supports hover information, zooming, and plot customization
- Can be used in Jupyter notebooks or exported to HTML
- Key functions:
  - `px.histogram()` - Interactive histograms
  - `px.scatter()` - Interactive scatter plots
  - `px.bar()` - Interactive bar charts
  - `px.box()` - Interactive box plots
  - `px.line()` - Interactive line charts
  - `px.choropleth()` - Interactive maps

## Chart Types and Use Cases

### Distribution Charts
1. **Histogram**
   - Shows the **distribution of a numerical variable**
   - Bins data into ranges and counts occurrences
   - Use when: Analyzing distribution shape, detecting skewness, identifying outliers
   - Example: `plt.hist(data)`, `sns.histplot(data)`, `px.histogram(data)`

2. **Box Plot (Box and Whisker)**
   - Shows **statistical summaries** (median, quartiles, outliers)
   - Displays distribution characteristics compactly
   - Use when: Comparing distributions, identifying outliers, examining spread
   - Example: `plt.boxplot(data)`, `sns.boxplot(data)`, `px.box(data)`

3. **Density Plot (KDE)**
   - Shows **smoothed distribution** of numerical data
   - Like a continuous histogram with a smoothing function
   - Use when: Visualizing distributions with smoother curves than histograms
   - Example: `sns.kdeplot(data)`, `px.histogram(data, marginal="kde")`

### Relationship Charts
1. **Scatter Plot**
   - Shows **relationship between two numerical variables**
   - Points represent individual data points
   - Use when: Identifying correlations, patterns, or clusters
   - Example: `plt.scatter(x, y)`, `sns.scatterplot(x, y)`, `px.scatter(data, x, y)`

2. **Bubble Chart**
   - Scatter plot with **varying point sizes** (third dimension)
   - Use when: Visualizing three numerical variables
   - Example: `plt.scatter(x, y, s=size)`, `sns.scatterplot(x, y, size=z)`, `px.scatter(data, x, y, size=z)`

3. **Heatmap**
   - Uses **color intensity** to represent values in a matrix
   - Often used for correlation matrices
   - Use when: Visualizing correlations or patterns in matrix data
   - Example: `sns.heatmap(data)`, `px.imshow(data)`

### Comparison Charts
1. **Bar Chart**
   - Shows **comparisons among discrete categories**
   - Use when: Comparing quantities across categories
   - Example: `plt.bar(x, height)`, `sns.barplot(x, y)`, `px.bar(data, x, y)`

2. **Grouped Bar Chart**
   - Compares **multiple series across categories**
   - Use when: Comparing groups within categories
   - Example: `px.histogram(data, x, color, barmode="group")`

3. **Stacked Bar Chart**
   - Shows **part-to-whole relationships** across categories
   - Use when: Showing composition changes across categories
   - Example: `px.histogram(data, x, color, barmode="stack")`

### Time Series Charts
1. **Line Chart**
   - Shows **trends over time** or ordered progression
   - Use when: Tracking changes over continuous intervals
   - Example: `plt.plot(x, y)`, `sns.lineplot(x, y)`, `px.line(data, x, y)`

2. **Area Chart**
   - Line chart with **filled area beneath**
   - Use when: Showing cumulative totals or volumes over time
   - Example: `plt.fill_between(x, y)`, `px.area(data, x, y)`

### Composition Charts
1. **Pie Chart**
   - Shows **proportions of a whole** as slices
   - Use when: Showing simple proportional relationships among few categories
   - Example: `plt.pie(sizes)`, `px.pie(data, values, names)`

2. **Sunburst Chart**
   - Shows **hierarchical data** as nested rings
   - Use when: Visualizing hierarchical relationships and proportions
   - Example: `px.sunburst(data, path, values)`

3. **Waffle Chart**
   - Shows **proportions as grid of squares**
   - Use when: Creating visually intuitive proportion displays
   - Example: Using `pywaffle` package: `Waffle(values=data)`

### Geographic Charts
1. **Choropleth Map**
   - Shows **data variations across geographic regions** using color
   - Use when: Visualizing data with geographical significance
   - Example: `px.choropleth(data, locations, color)`

2. **Scatter Geo**
   - Shows **data points on a map**
   - Use when: Plotting specific locations with additional data
   - Example: `px.scatter_geo(data, lat, lon, size, color)`

## Advanced Visualization Concepts

### Multi-Chart Layouts
1. **Subplots**
   - Multiple charts in **one figure**
   - Use when: Comparing different views of data side by side
   - Example: `plt.subplots(rows, cols)`, `make_subplots(rows, cols)`

2. **Facet Grids**
   - Creates **grid of plots** based on categorical variables
   - Use when: Analyzing same relationship across different subgroups
   - Example: `sns.FacetGrid(data, row, col)`, `px.scatter(data, facet_row, facet_col)`

3. **Scatter Matrix**
   - Shows **pairwise relationships** between multiple variables
   - Use when: Exploring relationships in multivariate data
   - Example: `sns.pairplot(data)`, `px.scatter_matrix(data, dimensions)`

### Plot Customization
1. **Color Palettes**
   - Use meaningful colors to enhance understanding
   - Consider colorblind-friendly palettes when appropriate
   - Example: `sns.set_palette()`, `color_discrete_sequence` in Plotly

2. **Styling**
   - Customize themes, fonts, grid lines, and backgrounds
   - Example: `sns.set_style()`, `plt.style.use()`, `template` in Plotly

3. **Annotations**
   - Add text, arrows, or shapes to highlight key insights
   - Example: `plt.text()`, `plt.annotate()`, `fig.add_annotation()` in Plotly

4. **Interactivity**
   - Add tooltips, zoom, pan, or selection capabilities
   - Primarily available in Plotly visualizations

## Best Practices for Data Visualization

1. **Choose the Right Chart Type**
   - Select visualization based on the story you want to tell
   - Consider your audience's familiarity with chart types

2. **Simplify and Focus**
   - Remove chart junk and unnecessary elements
   - Highlight the key message you want to convey

3. **Use Color Effectively**
   - Choose meaningful color schemes
   - Ensure sufficient contrast for readability
   - Be mindful of color-blind accessibility

4. **Label Clearly**
   - Add descriptive titles, axis labels, and legends
   - Consider adding data labels when appropriate

5. **Scale Appropriately**
   - Choose axis scales that don't distort the message
   - Consider whether to start axes at zero

6. **Tell a Story**
   - Organize visualizations in a logical flow
   - Add context and explanation where needed

## Code Structure for Effective Visualization

1. **Data Preparation**
   - Clean and transform data before visualization
   - Create aggregations if needed

2. **Base Plot Creation**
   - Set figure size and create basic plot

3. **Customization**
   - Add titles, labels, colors, and other styling elements

4. **Additional Elements**
   - Add annotations, reference lines, or highlights

5. **Display or Save**
   - Show the plot or save to file in appropriate format