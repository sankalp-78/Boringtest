# Boringtest

this is a readme for boringtest


PassengerName|BoardingLocation|Destination|Date|BookingStatus|Price
Ravi|Delhi|Mumbai|2025-09-10|Confirmed|1200
Sita|Chennai|Bangalore|2025-09-11|Pending|800
Arun|Kolkata|Delhi|2025-09-12|Confirmed|1500
Meera|Delhi|Goa|2025-09-15|Cancelled|950

awk -F '|' 'NR==1 || $5=="Confirmed"' passengers.txt

awk -F '|' -v OFS='|' '{ if ($1=="Ravi") $3="Pune"; print }' passengers.txt > updated_passengers.txt

awk -F '|' 'NR>1 && $5=="Confirmed" {sum+=$6} END{print "Total Revenue:", sum}' passengers.txt
