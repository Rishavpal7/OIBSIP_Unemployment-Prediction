# Unemployment-Prediction-
#Analysis of Unemployment state-wise


import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("Unemployment in India1.csv")
df
df.hist(figsize=(14,14))
plt.show
df.plot.scatter(x=" Estimated Unemployment Rate (%)", y=" Estimated Employed", alpha=0.5)
plt.show()
df.plot.scatter(x=" Estimated Unemployment Rate (%)", y=" Frequency", alpha=0.4)
plt.show()
df['total']=df.iloc[:,-34:].sum(axis=1)
df.head()
plt.xticks(rotation='vertical') 
plt.bar(x=" Frequency", height=" Estimated Unemployment Rate (%)", visible=True, width=0.4, bottom=None, align='center', data=df[:-200])
plt.show()
df.dtypes
data=df[:-200]
print(data)
import matplotlib.pyplot as plt

# Assuming you have your data stored in a DataFrame called 'df'

# Create a bar plot
plt.figure(figsize=(10, 6))  # Adjust the figure size if needed
plt.bar(x=df['Region'], height=df[' Estimated Unemployment Rate (%)'])

# Set the title and labels for the plot
plt.title('Estimated Unemployment Rate by Region')
plt.xlabel('Region')
plt.ylabel(' Estimated Unemployment Rate (%)')

# Rotate x-axis labels vertically
plt.xticks(rotation='vertical')

# Display the plot
plt.show()
plt.xticks(rotation='vertical') 
plt.bar(x="Andhra Pradesh",height=" Estimated Unemployment Rate (%)" ,width=0.1, bottom=None, align='center', data=df[:-200])
plt.xticks(rotation='vertical') 
plt.bar(x="Bihar",height=" Estimated Unemployment Rate (%)" ,width=0.2, align='center', color='Orange', data=df[:-20])
import matplotlib.pyplot as plt

# Assuming you have your data stored in a DataFrame called 'df'

# Create a bar plot
plt.figure(figsize=(10, 6))  # Adjust the figure size if needed
plt.bar(x=df['Region'], height=df[' Estimated Labour Participation Rate (%)'])

# Set the title and labels for the plot
plt.title(' Estimated Labour Participation (%)')
plt.xlabel('Region')
plt.ylabel(' Estimated Labour Participation Rate (%)')

# Rotate x-axis labels vertically
plt.xticks(rotation='vertical')

# Display the plot
plt.show()
x=df.loc[df["Region"]=="West Bengal"]
print(x[" Estimated Unemployment Rate (%)"].sum())
x=df.loc[df["Region"]=="Andhra Pradesh"]
print(x[" Estimated Unemployment Rate (%)"].sum())
x=df.loc[df["Region"]=="Assam"]
print(x[" Estimated Unemployment Rate (%)"].sum())
x=df.loc[df["Region"]=="Bihar"]
print(x[" Estimated Unemployment Rate (%)"].sum())
x=df.loc[df["Region"]=="Goa"]
print(x[" Estimated Unemployment Rate (%)"].sum())
sns.pairplot(df)
x = input("Enter a region : ")
rslt_df = df[df['Region'] == x]
rslt_df
sns.heatmap(df.corr(),annot=True)
plt.xticks(rotation='vertical')
sns.lineplot(x=df['Region'], y=df[' Estimated Unemployment Rate (%)'], color = 'green',data=df)
plt.xticks(rotation='vertical')
sns.scatterplot(x=df[' Date'], y=df['Region'], color = 'green',data=df)
grouped = df.groupby('Region').sum()
grouped.plot(kind='line', figsize=(30, 10))
plt.title("Trend of Unemployment")
plt.xlabel("Region")
plt.ylabel("Number ")
plt.show()
pd.pivot_table(data = df, values =' Estimated Unemployment Rate (%)', index =['Region',' Date', 'Area'],aggfunc = max)
pq2 = df.loc[df['Region']=='Bihar']
plt.figure(figsize=(20,10))
plt.title("Estimated Unemployment Rate of Bihar on particular dates")
sns.barplot(data=pq2,y=" Estimated Unemployment Rate (%)",x=" Date",estimator=sum,palette="viridis")
pq2 = df.loc[df['Region']=='Bihar']
plt.figure(figsize=(20,10))
plt.title("Estimated Unemployment Rate of Bihar on the basis of area")
sns.barplot(data=pq2,y=" Estimated Unemployment Rate (%)",x="Area",estimator=sum,palette="viridis")
pq2 = df.loc[df['Region']=='Goa']
plt.figure(figsize=(20,10))
plt.title("Estimated Unemployment Rate of Goa on particular dates")
sns.barplot(data=pq2,y=" Estimated Unemployment Rate (%)",x=" Date",estimator=sum,palette="viridis")
pq2 = df.loc[df['Region']=='Goa']
plt.figure(figsize=(20,10))
plt.title("Estimated Unemployment Rate of Goa on the basis of area")
sns.barplot(data=pq2,y=" Estimated Unemployment Rate (%)",x="Area",estimator=sum,palette="viridis")
pq2 = df.loc[df['Region']=='Assam']
plt.figure(figsize=(20,10))
plt.title("Estimated Unemployment Rate of Assam on the basis of area")
sns.barplot(data=pq2,y=" Estimated Unemployment Rate (%)",x="Area",estimator=sum,palette="viridis")
pq2 = df.loc[df['Region']=='Assam']
plt.figure(figsize=(20,10))
plt.title("Estimated Unemployment Rate of Assam on particular dates")
sns.barplot(data=pq2,y=" Estimated Unemployment Rate (%)",x=" Date",estimator=sum,palette="viridis")
Bihar = [9.27,10.2,13.44,11,8.87,12.47,12.4,10.16]
Goa = [5.45,10.98,1.98,3.61,7.21,23.71,3.54,5.38]
n=8
r = np.arange(n)
width =0.4
plt.figure(figsize=(10, 6))
plt.bar(r,Bihar, color = 'b',width = width, edgecolor = 'black',label='BIHAR')
plt.bar(r + width, Goa, color = 'g',width = width, edgecolor = 'black',label='GOA')

plt.xlabel("DATE")
plt.ylabel("UNEMPLOYMENT RATE")
plt.title("Comparison of Unemployment of Bihar VS Goa")

# plt.grid(linestyle='--')
plt.xticks(r + width/2,[' 31-05-2019',
 '30-06-2019',
 '31-07-2019',
 '31-08-2019',
 '30-09-2019',
 '31-10-2019',
 '30-11-2019',
 '31-12-2019',])
plt.legend()
plt.show()
Assam = [4.29,
5.08,
4.26,
5.79,
4.46,
4.65,
4.66]
Telangana = [2.23,
5.92,
2.45,
1.4,
5.49,
7.29,
6.47]
Bihar = [9.27,10.2,13.44,11,8.87,12.47,12.4]
Goa = [5.45,10.98,1.98,3.61,7.21,23.71,3.54]
n=7
r = np.arange(n)
width =0.4
plt.figure(figsize=(20, 10))
plt.bar(r,Assam, color = 'r',width = width, edgecolor = 'black',label='ASSAM')
plt.bar(r + width,Telangana, color = 'orange',width = width, edgecolor = 'black',label='TELANGANA')
plt.bar(r + width+width, Bihar, color = 'g',width = width, edgecolor = 'black',label='BIHAR')
plt.bar(r + width+width+width, Goa, color = 'b',width = width, edgecolor = 'black',label='GOA')

plt.xlabel("DATE")
plt.ylabel("UNEMPLOYMENT RATE (%)")
plt.title("Comparison of Unemployment Rate(%) of ASSAM VS TELANGANA VS BIHAR VS GOA")

# plt.grid(linestyle='--')
plt.xticks(r + width/2,[' 31-05-2019',
 '30-06-2019',
 '31-07-2019',
 '31-08-2019',
 '30-09-2019',
 '31-10-2019',
 '30-11-2019'])
plt.legend()
plt.show()
y = np.array([4.29,57.39])
mylabels = [" Estimated Unemployment Rate (%)"," Estimated Labour Participation Rate (%)"]

plt.pie(y, labels= mylabels)
plt.legend(title="31/05/ASSAM 2019", fontsize=8)
plt.show() 
y = np.array([23.92,41.4])
mylabels = [" Estimated Unemployment Rate (%)"," Estimated Labour Participation Rate (%)"]
plt.title("Pie Chart Analysis of Estimated Unemployement and Estimated Labour Participation of Haryana on 31/03/2020")
plt.pie(y, labels= mylabels)
plt.legend(title="Haryana on 31/03/2020", fontsize=5)
plt.show() 
y = np.array([4.59,36.36])
mylabels = [" Estimated Unemployment Rate (%)"," Estimated Labour Participation Rate (%)"]
plt.title("Pie Chart Analysis of Estimated Unemployement and Estimated Labour Participation of Odisha on  30-06-2020")
plt.pie(y, labels= mylabels)
plt.legend(title="Odisha on  30-06-2020", fontsize=5)
plt.show() 
y = np.array([26.53,63.02])
mylabels = [" Estimated Unemployment Rate (%)"," Estimated Labour Participation Rate (%)"]
plt.title("Pie Chart Analysis of Estimated Unemployement and Estimated Labour Participation of Tripura on 31-12-2019")
plt.pie(y, labels= mylabels)
plt.legend(title="Tripura on 31-12-2019", fontsize=5)
plt.show() 







