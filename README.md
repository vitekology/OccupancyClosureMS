***README: Data for "Thinking beyond the closure assumption: designing surveys for estimating biological truth with occupancy models"***

Jonathon J. Valente, Vitek Jirinec, Matthias Leu

**Introduction**

This repository contains the dataset and R code associated with the manuscript: "Thinking beyond the closure assumption: designing surveys for estimating biological truth with occupancy models." The study focuses on analyzing the occupancy of Wood Thrush (Hylocichla mustelina) using telemetry data, point count protocols, and individual-based modeling.

**Dataset description**

The dataset includes several CSV files and an RData file used in the study. Below is a detailed description of each file.

**Data files**

    capLocs.csv: Contains capture location data for individual Wood Thrush males.
    estDepDates.csv: Provides estimated departure dates for the tracked birds.
    SimulationStart.RData: An RData file that initializes the simulations used in the analysis.
    wothFates.csv: Contains information on the fate of the Wood Thrush individuals tracked during the study.
    wothLocations.csv: Provides spatial location data for each tracked Wood Thrush over the study period.

**Data structure**

Each data file is organized as follows:

capLocs.csv

    Columns:
        bird_id: Unique identifier for each tracked Wood Thrush.
        capDate: Date of capture.
        capX, capY: Capture location coordinates (UTM).

estDepDates.csv

    Columns:
        bird_id: Unique identifier for each tracked Wood Thrush.
        departure_dt: The date when the bird is estimated to have departed from its territory.

SimulationStart.RData

    Description: This RData file contains the initialization parameters for the individual-based simulations used in the manuscript. To use this file, load it in R with the appropriate function.
    Contents: Parameters related to the IBM simulations, including initial positions, movement models, and breeding season durations.

wothFates.csv

    Columns:
        check: The date of telemetry check - the first one is capture date.
        bird_id: Unique identifier for each tracked Wood Thrush.
        int: The number of the current telemetry check, labeled consecutively starting with 2 (1 is capture).
        t: The number of days since last telemetry check.
        age: The number of days since trapping of that individual.
        sday: Season day (days trapping of first bird that year) - accounts for differences between the two sampling years.
        fate: Status indicating the fate of the individual (1 = in current territory, 0 = departed).

wothLocations.csv

    Columns:
        bird_id: Unique identifier for each tracked Wood Thrush.
        telem_pt: Rank of telemetry location.
        pt_id: Unique telemetry point identifier.
        dt: Timestamp.
        latitude: latitude
        longitude: longitude
        Y: Location UTM Y.
        X: Location UTM X.
        interval: Interval (s).
        T: Time (s).
        distMoved: Distance moved since the last location (m).
        speed: Speed.
        daysSinceCap: The number of days since capture.
        distFromCap: Distance from capture location (m).
        territory: Territory number.
                
