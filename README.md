# Data-Analyst
# This Python 3 environment comes with many helpful analytics libraries installed
# It is defined by the kaggle/python Docker image: https://github.com/kaggle/docker-python
# For example, here's several helpful packages to load

import numpy as np # linear algebra
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)

# Input data files are available in the read-only "../input/" directory
# For example, running this (by clicking run or pressing Shift+Enter) will list all files under the input directory

import os
for dirname, _, filenames in os.walk('/kaggle/input'):
    for filename in filenames:
        print(os.path.join(dirname, filename))

# You can write up to 20GB to the current directory (/kaggle/working/) that gets preserved as output when you create a version using "Save & Run All" 
# You can also write temporary files to /kaggle/temp/, but they won't be saved outside of the current session

df=pd.read_csv("/kaggle/input/job-description-dataset/job_descriptions.csv")
df.head(2)

df.columns

df.describe()

df.info()

df.shape

df.Qualifications

df.Company_Profile

df.rename(columns={'Job Id':'Job_Id','Salary Range':'Salary_Range','Work Type':'Work Type','Company Size':'Company Size','Job Posting Date':'Job_Posting_Date','Contact person':'Contact_Person','Job Title':'Job_Title','Job Portal':'Job_Portal','Job Description':'Job_Description','Company Profile':'Company_Profile'},inplace=True)

df.head(3)

df.columns

df.isnull().sum()

df.shape

df.dropna(inplace=True)

df.isnull().sum()

df.drop_duplicates(inplace=True)
