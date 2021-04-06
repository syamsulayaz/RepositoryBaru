# RepositoryBaru
import pandas as pd

df_sheet1 = pd.read_excel("Data000_Excel.xlsx",sheet_name='Sheet01')
df_sheet1

df_sheet2 = pd.read_excel("Data000_Excel.xlsx",sheet_name='Sheet02')
df_sheet2

df_sheet1.iloc[[1]]

df_sheet1.loc["Column_1"]

lst_s1_cl1 = df_sheet1["Column_1"].T.tolist()

type(lst_s1_cl1)

lst_s1_cl2 = df_sheet1["Column_2"].T.tolist()
type(lst_s1_cl2)

print(lst_s1_cl2)

import numpy as np
np.mean(lst_s1_cl1)

df_sheet1["Column_1"].describe()

import matplotlib.pyplot as plt

plt.hist(lst_s1_cl1)

plt.title("Data Column 1")
plt.xlabel("month")
plt.ylabel("US Dollar")
plt.plot(lst_s1_cl1)

plt.title("Data Column 1 & ")
plt.xlabel("month")
plt.ylabel("US Dollar")
plt.plot(lst_s1_cl1,lst_s1_cl2)

print(lst_s1_cl1[0:100])

len(lst_s1_cl1[0:100])

plt.title("Data Column 1 & 2")
plt.xlabel("Column 1")
plt.ylabel("Column 2")
plt.plot(lst_s1_cl1[0:100],lst_s1_cl2[0:100])

df_sheet1["Column_3"]

lst_s1_c3 = df_sheet1["Column_3"].tolist()

plt.title("Data Column 1 ")
plt.xlabel("month")
plt.ylabel("US Dollar")
plt.plot(lst_s1_cl1[0:100],lst_s1_c3[0:100])

plt.title("Data Column 1 ")
plt.xlabel("month")
plt.ylabel("US Dollar")
plt.plot(lst_s1_c3[0:100],lst_s1_cl1[0:100])

df_sheet1[['Column_1','Column_2']].corr()

df_sheet1['Column_1'][0:50]

df_corr1dan2 = pd.DataFrame(data=np.c_[lst_s1_cl1[0:50],lst_s1_cl2[50:100]],
                           columns=['Column 1','Column 2'])
df_corr1dan2

df_corr1dan2.corr()

import matplotlib.pyplot as plt

plt.matshow(df_corr1dan2.corr())
plt.show()
plt.matshow(df_sheet1.corr())
plt.show()

df_sheet1.drop(['NO'])
corr = df_sheet1.corr()
corr.style.background_gradient(cmap='YlGnBu')
                           

