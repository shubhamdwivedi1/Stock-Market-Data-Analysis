# Stock-Market-Data-Analysis
Stock Analysis Hands On Stocks Data Retrieving from Yahoo Finance(Advanced Micro Devices,
Inc. (AMD), IBM, NIVIDIA ,QualComm and Intel Corporation)
From 31-Dec-2013 to 03-Sept-2019(Historical Data)

ReSampling Data (Monthly,Quaterly,Yearly)

Moving Windows (How stock performed)

Volatility (Which Stock is more)

Importing Dataset from Yahoo by Using Pandas DataReader

Time Series Data Visualization

Data Visualisatin Using Subplots


                             Time Series Data Visualization 
                             
                             
plt.plot(ibm.index, ibm['Adj Close'])
plt.gca().xaxis.set_major_formatter(mdates.DateFormatter('%Y'))
plt.gca().xaxis.set_major_locator(mdates.YearLocator())
plt.grid(True)
plt.xticks(rotation=90)
plt.show()


# SubPlots
f,ax = plt.subplots(2,2,figsize=(10,10),sharex=True)
f.gca().xaxis.set_major_formatter(mdates.DateFormatter('%Y'))
f.gca().xaxis.set_major_locator(mdates.YearLocator())

ax[0,0].plot(nvda.index, nvda['Adj Close'],color='r')
ax[0,0].grid(True)
ax[0,0].tick_params(labelrotation=90)
ax[0,0].set_title('NVIDIA');

ax[0,1].plot(intc.index, intc['Adj Close'],color='g')
ax[0,1].grid(True)
ax[0,1].tick_params(labelrotation=90)
ax[0,1].set_title('INTEL');

ax[1,0].plot(qcom.index, qcom['Adj Close'],color='b')
ax[1,0].grid(True)
ax[1,0].tick_params(labelrotation=90)
ax[1,0].set_title('QUALCOMM');

ax[1,1].plot(amd1.index, amd1['Adj Close'],color='y')
ax[1,1].grid(True)
ax[1,1].tick_params(labelrotation=90)
ax[1,1].set_title('AMD');

