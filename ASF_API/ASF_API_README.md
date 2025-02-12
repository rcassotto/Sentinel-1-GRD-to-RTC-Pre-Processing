### Overview
The ASF_API contains 2 sample python scripts to pull Sentinel-1 data from the Alaska SAR Facility (ASF)
archive. The script creates a user defined directory, retrieves Earth Data login credentials from the user's 
bachrc file, downloads the data the user defined directory, and creates a log file using the standard output. 

### Setup 
1) Create a dedicated Anaconda environment (e.g. conda create -n asf_api python=3.7.x). As of today 10/20/2022, 
   python versions 3.7 and 3.8 are compatible; v3.10 was not. 
   
2) Install ASF's python wrapper for its API, asf_search (conda install -c conda-forge asf_search)  
Ref: https://docs.asf.alaska.edu/asf_search/basics/ 

3) Register for an Earth Data account (it's free!)

4) Add your Earth Data account credentials to your bashrc file by executing the following commands in a terminal:      
        _(export ASF_API_PASS=&lt;password>)_   
         export ASF_API_USER=&lt;username>  
   _Note &lt;username> and &lt;password> should be replaced with the Earth Data account credentials
   without angled brackets but with single quotes (‘ ‘)._

### Execution
1) Customize the sentinel_asf_searchAPI_XXXXXX.py for desired inputs. See https://docs.asf.alaska.edu/asf_search/searching/
   for a full list of keywords. 
   
2) activate conda environment with asf_search library (e.g. conda activate asf_api)

3) Call the script: python sentinel_asf_searchAPI_XXXXXX.py

Dependencies:
- asf_search library
- Earth Data account (it's free)



