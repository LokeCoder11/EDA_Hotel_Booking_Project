# EDA_Hotel_Booking_Project:
---

**Hotel Booking Exploratory Data Analysis (EDA)**

**1. Objective**

The primary objective of this project is to conduct a comprehensive Exploratory Data Analysis (EDA) on a provided hotel bookings dataset. This analysis aims to ascertain general trends prevalent in hotel booking patterns and to investigate the interrelationships between various factors that govern these bookings.

**2. Dataset Description**

The dataset utilized for this analysis contains detailed booking information for two distinct hotel categories: a City Hotel and a Resort Hotel. The dataset is structured with the following features:

* `hotel`: Categorical variable indicating the type of hotel (Resort Hotel or City Hotel).
* `is_canceled`: Binary indicator variable signifying whether a booking was canceled (1) or not (0).
* `lead_time`: Integer representing the number of days between the booking entry date into the Property Management System (PMS) and the scheduled arrival date.
* `arrival_date_year`: Year of the scheduled arrival date.
* `arrival_date_month`: Month of the scheduled arrival date.
* `arrival_date_week_number`: Week number of the year corresponding to the arrival date.
* `arrival_date_day_of_month`: Day of the month corresponding to the arrival date.
* `stays_in_weekend_nights`: Number of weekend nights (Saturday or Sunday) included in the booking duration.
* `stays_in_week_nights`: Number of week nights (Monday to Friday) included in the booking duration.
* `adults`: Number of adult guests included in the booking.
* `children`: Number of children included in the booking.
* `babies`: Number of infants included in the booking.
* `meal`: Categorical variable specifying the type of meal package booked, presented according to standard hospitality categories.
* `country`: The country of origin of the guest.
* `market_segment`: Designation of the market segment the booking originated from. 'TA' denotes Travel Agents, and 'TO' denotes Tour Operators.
* `distribution_channel`: The channel through which the booking was made. 'TA' denotes Travel Agents, and 'TO' denotes Tour Operators.
* `is_repeated_guest`: Binary indicator variable signifying whether the booking was made by a repeat guest (1) or a new guest (0).
* `previous_cancellations`: The count of previous bookings by the same customer that were canceled prior to the current booking.
* `previous_bookings_not_canceled`: The count of previous bookings by the same customer that were not canceled prior to the current booking.
* `reserved_room_type`: Coded identifier for the type of room originally reserved. Codes are used for anonymity.
* `assigned_room_type`: Coded identifier for the type of room assigned to the booking.
* `booking_changes`: The total number of amendments or modifications made to the booking from its entry into the PMS until check-in or cancellation.
* `deposit_type`: Indicator specifying the nature of the deposit made to secure the booking.
* `agent`: Identifier for the travel agency associated with the booking.
* `company`: Identifier for the company or entity responsible for the booking payment.
* `days_in_waiting_list`: The number of days the booking remained in a waiting list before confirmation.
* `customer_type`: Categorical variable specifying the type of customer, assuming one of four predefined categories.
* `adr`: Average Daily Rate, calculated as the sum of all lodging transactions divided by the total number of staying nights.
* `required_car_parking_spaces`: The number of car parking spaces requested by the customer.
* `total_of_special_requests`: The total count of special requests made by the customer (e.g., specific bed configuration, room location).
* `reservation_status`: The final status of the reservation (Canceled, Check-Out, No-Show).
* `reservation_status_date`: The date on which the final reservation status was set, providing a timestamp for cancellation or check-out.

The dataset comprises a total of 119,390 rows and 32 columns.

**3. Data Understanding and Preparation**

Initial steps involved gaining a comprehensive understanding of the dataset structure and content. This phase included:

* Inspecting dataset information to identify data types and potential issues.
* Identifying and quantifying duplicate records.
* Assessing the extent and distribution of missing or null values.
* Examining the unique values for each variable to understand their range and categories.

The data preparation (wrangling) process entailed:

* Determining the year and month with the highest volume of customer arrivals.
* Analyzing categorical variables such as `customer_type`, `reserved_room_type`, `deposit_type`, and `is_canceled`.
* Quantifying the number of bookings that underwent modifications.
* Removing duplicate entries to ensure data integrity.
* Confirming unique values post-cleaning.
* Evaluating the ratio of different hotel types.
* Deriving new features such as `total_staying_days` and `total_people_stays` by aggregating existing columns.
* Addressing outliers, potentially using visualization techniques like box plots, to improve data distribution for analysis.

**4. Research Questions**

The EDA was guided by the following key research questions:

* Which customer types exhibit the highest booking frequency?
* Which room type demonstrates the highest demand, and concurrently, which room type generates the highest Average Daily Rate (ADR)?
* Which distribution channel is most effective in bringing high revenue-generating deals for hotels?
* Which significant distribution channel is associated with the highest booking cancellation percentage?
* What is the booking trend observed within a typical month?
* Which hotel type exhibits a higher booking ratio?
* What is the preferred length of stay when compared across different customer types?
* In which specific year did the highest number of bookings occur for both hotel types?
* From which country do the majority of guests originate?
* In which calendar month did the highest volume of bookings take place?
* Which market segments have the highest incidence of booking followed by cancellation?
* Which customer segment (e.g., Couples, Single, Group) has the highest booking volume?
* Which meal type is the most frequently preferred by customers?
* What are the correlations among different variables within the dataset?
* Which booking characteristic or segment is associated with the highest ADR?

**5. Analytical Approach and Visualizations**

The analytical approach primarily involved leveraging the Matplotlib and Seaborn libraries in Python for data visualization. Both univariate and bivariate analyses were conducted using a variety of graphical representations, including:

* Bar Plots
* Histograms
* Scatter Plots
* Pie Charts
* Line Plots
* Heatmaps
* Box Plots
* Pair Plots

These visualizations were instrumental in identifying patterns, distributions, and relationships within the dataset to support the drawing of conclusions.

**6. Key Findings and Conclusions**

The exploratory data analysis yielded several important findings:

* Approximately 60% of the bookings are for the City Hotel, while 40% are for the Resort Hotel, indicating a higher occupancy rate for the City Hotel. The overall Average Daily Rate (ADR) for the City Hotel is marginally higher than that of the Resort Hotel.
* The majority of guests typically stay for less than 5 days. For longer durations, the Resort Hotel appears to be the preferred choice.
* Both hotel types exhibit notably high booking cancellation rates. Furthermore, a very low percentage of guests return for subsequent bookings, specifically less than 3% for the City Hotel and 5% for the Resort Hotel.
* The predominant origin of guests is from European countries, with Portugal contributing the highest volume of guests.
* Guests utilize a variety of channels for booking, with the TA/TO (Travel Agent/Tour Operator) channel being the most preferred.
* Almost 30% of bookings made through the TA/TO channel are subsequently canceled.
* July and August emerge as the busiest and most profitable months for both hotel types.
* Couples represent the most frequent guest configuration. Hotels could potentially tailor services or packages to cater to the needs of couples to enhance revenue.
* From a customer perspective, longer stays (exceeding 15 days) can potentially result in more favorable deals in terms of a lower average daily rate.
* A higher lead time (number of days between booking and arrival) is correlated with an increased probability of cancellation. Additionally, a history of previous cancellations by a customer significantly elevates the likelihood of future cancellations.

**7. Challenges Encountered**

Several challenges were encountered during the EDA process:

* The presence of a substantial volume of duplicate records required rigorous data cleaning procedures.
* Data was present in inconsistent or incorrect data type formats, necessitating type conversion.
* Selecting the most appropriate visualization techniques to effectively represent complex patterns and relationships proved challenging at times.
* The dataset contained a considerable number of missing (null) values that required careful handling or imputation strategies.
