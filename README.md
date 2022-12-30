# **Hotel Bookings Exploratory Data Analysis**
 
## **Objective**

We are provided with a hotel bookings dataset.Out main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

## **Dataset**
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.

• Total number of rows in data: 119390
 
• Total number of columns: 32

## **Data Cleaning and Feature Engineering**

**(1) Removing Duplicate rows**

All duplicate rows were dropped.

**(2) Handling null values** 

• Null values in columns company and agent were replaced by 0. 

• Null values in column country were replaced by 'others'.

• Null values in column children were replaced by the mean of the column.

**(3) Converting columns to appropriate data types** 

• Changed data type of children, company, agent to int type. 

• Changed data type of reservation_status_date to date type.

**(4) Removing outliers** 

• One outlier was found in the adr column. Simply dropped it.

**(5) Creating new columns** 

• Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights. 

• Created new column total_people by adding adults+children+babies.

## **Exploratory Data Analysis**

Performed EDA and tried answering the following questions:

Q1.Which agent makes most no. of bookings?

Q2.Which meal type is most preffered meal of customers

Q3.Which is the most common channel for booking hotels?

Q4.What is preffered stay in eacg hotel?

Q5.What is percentage of bookings in each hotel?

Q6.Which hotel has longer waiting time?

Q7.Which hotel has higher bookings cancellation rate?

Q8.Which room type is in most demand and which room type generates highest adr?

Q9.From where most guests are coming?

Q10.which hotel seems to make more revenue?

Q11.Which hotel has higher lead time?

Q12.Which significant distribution channel has highest cancellation percentage?

Q13.which channel is mostly used for early booking of hotels?

Q14.which channel has longer average waiting time?


Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

1)Bar Plot.

2)Histogram.

3)Scatter Plot.

4)Pie Chart.

5)Line Plot.

6)Heatmap.

7)Box Plot


 
 ## **Conclusion**
 - (1) Agent no. 9 has made most no. of bookings. 
 - (2)BB (bed and breakfast) is the most prefered type of meal in hotel.
- (3) TA/TO is the most common channel for booking hotels.
- (4)  Most common stay length is less than 4 days and generally people prefer City hotel for short stay, but for long stays, Resort Hotel is preferred.
- (5) percentage of booking in City Hotel is 60% and in Resort Hotel is 40%.
- (6) City hotel has longer waiing time than Resort Hotel.
- (7) City Hotel has 30% booking cancalation rate.
- (8) Most demanded room type is A, but better adr rooms are of type H, G and C also.
- (9) Most of the guest are from Portugal.
- (10) City hotel seems to be making slightly more revenue.
- (11) City Hotel has higher lead time than Resort Hotel.
- (12) TA/TO channel has highest cancellation percentage.
- (13)TA/TO is mostly used for planning hotel visits ahead of time.but sudden visits other medium are most preferred.
- (14) while booking via TA/TO one may have to wait a little longer to confirm booking of rooms.
- (15) (1)Total stay length and lead time have slight correlation. This may means that for longer hotel stays people generally plan little before the the actual arrival 
- (2).adr is slightly correlated with total_people, which makes sense as more no. of people means more revenue, therefore more adr.

- (16)(1).A pairs plot allows us to see both distribution of single variables relationships between two variables. Pair plots are a great method to identify trends for follow-up analysis and, fortunately, are easily implemented in Python.

(2)for example.the left-most plot in the second row shows the scatter plot of tip versus total_bill.it shows the relation between two variables in sysmatic way.

(3)just like that the other variables of graphs shows the relation between the two variables like.

(4)y-axis(total_bill) and x-axis(total_bill): total_bill relation with total_bill y-axis(total_bill) and x-axis(tip) total_bill relation with tip y-axis(total_bill) and x-axis(size) : total_bill relation with size

(5)y-axis(tip) and x-axis(total_bill) : tip relation with total_bill y-axis(tipl) and x-axis(tip) : tip relation with tip y-axis(tip) and x-axis(size) : tip relation with size

(6)y-axis(size) and x-axis(total_bill) : size relation with total_bill y-axis(size) and x-axis(tip) : size relation with tip y-axis(size) and x-axis(size) : size relation with size

And many more conclusions.


## **Challenges**
(1) There was a lot of duplicate data.

(2) Data was present in wrong datatype format.

(3) Choosing appropriate visualization techniques to use was difficult.

(4) A lot of null values were there in the dataset.
