# Bodo Examples

Welcome to Bodo examples! These are adapted from the [bodo.ai example repository](https://github.com/Bodo-inc/Bodo-examples).

## Examples and corresponding data generation

Many of the data generation scripts and example scripts can take in optional arguments. 
`python path/script.py --help` shows the usage.

By default all examples and data generation scripts can be run from home directory without any changes. Otherwise, make sure to change path of data files.

For more information on data generation and examples, please see the docstring at the top of each python script.

>**Note** Bodo works best on huge datasets, which can take some time to download.

- [Kernel Density Estimation](examples/kernel_density_estimation.py)
  - [data generation](data/kde_datagen.py)

- [Intraday Mean](examples/intraday_mean.py)
  - [data generation](data/stock_data_read.py)

- [Beer Reviews](examples/beer-reviews/beer-reviews.py)

- [NYC Parking Tickets](examples/nyc-parking/nyc-parking.py)

- [NYC Taxi](examples/nyc-taxi):
    - [Daily Pickups](examples/nyc-taxi/get_daily_pickups.py)
    - [JFK Hourly Pickups](examples/nyc-taxi/jfk_hourly_pickups.py)
    - [Monthly Travel Times](examples/nyc-taxi/monthly_taxi_travel_times.py)
    - [Weekday Pickup and Dropoff](examples/nyc-taxi/weekday_taxi_trips_by_pickup_and_dropoff.py)

- [Monte Carlo Pi Calculation](examples/miscellaneous/pi.py)

- [k-means](examples/miscellaneous/k-means.py)
  - [data generation](data/logistic_regression_datagen.py)

- [Linear Regression](examples/miscellaneous/linear_regression.py)
  - [data generation](data/linear_regression_datagen.py)

- [Logistic Regression](examples/miscellaneous/logistic_regression.py)
  - [data generation](data/logistic_regression_datagen.py)

## Try the examples

An example performing beer reviews example:

    # run example on 8 cores
    mpiexec -n 8 python examples/beer-reviews/beer-reviews.py

An example performing Monte Carlo Pi Calculation:

    # run the example on a single core
    python examples/pi.py
    # run the example on 8 cores
    mpiexec -n 8 python examples/pi.py
 
An example performing linear regression:

	# generate data
	python data/linear_regression_datagen.py
	# run example on 8 cores
	mpiexec -n 8 python examples/linear_regression.py


---------------------------
More documentation can be found at http://docs.bodo.ai.

Bodo tutorial can be found [here](https://github.com/Bodo-inc/Bodo-tutorial).