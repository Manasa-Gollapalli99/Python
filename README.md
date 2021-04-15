# Python
import numpy as np
import pandas as pd
# A dictionary with list as values
sample_dict = { 'S1': [10, 20, np.NaN, np.NaN],
                'S2': [5, np.NaN, np.NaN, 29],
                'S3': [15, np.NaN, np.NaN, 11],
                'S4': [21, 22, 23, 25],
                'Subjects': ['Maths', 'Finance', 'History', 'Geography']}
# Create a DataFrame from dictionary
df = pd.DataFrame(sample_dict)
# Set column 'Subjects' as Index of DataFrame
df = df.set_index('Subjects')
print(df)
mean_value=df['S2'].mean()
print('Mean of values in column S2:')
print(mean_value)
df['S2'].fillna(value=df['S2'].mean(), inplace=True)
print('Updated Dataframe:')
print(df)
df.fillna(value=df['S2'].mean(), inplace=True)
print('Updated Dataframe:')
print(df)
