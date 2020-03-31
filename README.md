# shashivardhan-projectCar-avail: semaphore := 0
Car-taken: semaphore := 0
Car-filled: semaphore := 0
Passenger-released : semaphore := 0
Passenger process code
Co-begin(I := 1 to num-passengers)
Do true ->
#wander around museum until ready to take a ride
P(car-avail);
V(car-taken);
P(passenger-released)
Od
Co-end
Car process code
Do true ->
V(car-avail)
P(car-taken)
V(car-filled)
Travel around the park until ride is done
V(passenger-released
Od
Co-end
