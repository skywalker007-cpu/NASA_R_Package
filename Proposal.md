# Project Proposal: An R Package with functions using NASA API

## 1. Project Title
**nasaR: An R Package for Accessing NASA's Space Data**

## 2. Team Members
- Zetian Zhao
- Litao Zheng
- Haoxiang Xu

## 3. API Selection
**API Name:** NASA Open APIs  
**Why choose this API?**  
We use NASA's open APIs because they contain a wealth of scientific information, including real-time images of space, planetary research information, and asteroid tracking information. In addition, the APIs have the tremendous ability to create data visualizations that serve educational purposes by making space science accessible. Thus, using this package, innovative links can be made between astronomy and statistical analysis using R.

## 4. Project Objectives
The `nasaR` package aims to:  
- Provide intuitive functions to access NASA’s Mars Rover Photos, Astronomy Picture of the Day (APOD), and Near-Earth Object (NEO) data.  
- Offer user-friendly data visualization tools for plotting space-related information.  
- Guarantee graceful error handling and comprehensive documentation to enhance usability for R users.

## 5. Expected Functions & Features
The package will include the following key functions:  
- **`get_apod()`**: Fetches the Astronomy Picture of the Day, including the image and its description.  
- **`get_mars_photos()`**: Retrieves recent images captured by the Rover on Mars.  
- **`get_neo_data()`**: Gain details about Near-Earth Objects and generates plots of their speed vs. distance.  
- **`get_earth_image()`**: Retrieves NASA satellite imagery based on user-input such as specific latitude and longitude coordinates.

## 6. Data Output and Visualization
Users will interact with the data as follows:  
- **APOD**: Returns the daily image about the sapce along with a descriptive caption in a clean format.  
- **Mars Rover**: Displays an image gallery of recent photos from the Curiosity Rover.  
- **Near-Earth Objects**: Produces interactive plots (e.g., asteroid sizes, speeds) using `ggplot2`.  
- **Earth Imagery**: Outputs satellite images tied to geographic coordinates, with options for customization.

## 7. Package Design & Implementation
- **Development Plan**:  
  - Use `httr` and `jsonlite` for API calls to retrieve and parse NASA data.  
  - Leverage `ggplot2` for creating high-quality visualizations.  
- **Testing**: 
  - Implement **unit tests** by using the `testthat` package.
  - Exerting the `vcr` package for the **integration tests**.
  - Both types of test ensure the package's reliability and accuracy.  
- **Version Control**: 
  - Host the project on a GitHub repository, utilizing pull requests for collaborative development.

## 8. Expected Challenges & Solutions
- **Challenge**: NASA APIs define hourly request limits.  
  **Solution**: Implement caching mechanisms to store responses locally and handle rate limits gracefully to solve the problem.

## 9. Timeline & Milestones
- **Week 1**:  
  - Set up package structure, test API connectivity, and implement `get_apod()` and `get_mars_photos()`.  
  - Begin basic unit tests with `testthat`.  
- **Week 2**:  
  - Implement `get_neo_data()` and `get_earth_image()` with visualizations.  
  - Add integration tests with `vcr`, finalize error handling, and write concise documentation.

## 10. Conclusion
The `nasaR` package will enable `R` users, from researchers to students, to easily explore the vast amount of space data provided by NASA. By integrating easy-to-use features and useful visualizations, it will facilitate learning and curiosity-driven inquiry in areas such as space science.

---
*Generated on March 04, 2025*