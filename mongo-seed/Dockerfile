FROM mongo

COPY svtest.json /svtest.json
COPY googleCal.json /googleCal.json
COPY mdpf.json /mdpf.json
COPY mdwc.json /mdwc.json
COPY empty.json /empty.json
COPY house.json /house.json
COPY person.json /person.json
COPY truck.json /truck.json
COPY vehicle.json /vehicle.json
COPY svtest.json /svtest.json

CMD mongoimport --host mongodb --db semantic_vocabs --collection test --type json --file /svtest.json --jsonArray && \
 mongoimport --host mongodb --db google_cal --collection auth --type json --file /googleCal.json --jsonArray && \
 mongoimport --host mongodb --db coaas_situation --collection situations --type json --file /empty.json --jsonArray && \
 mongoimport --host mongodb --db coaas_subscriptions --collection subscriptionsts --type json --file /empty.json --jsonArray && \
 mongoimport --host mongodb --db mydb --collection ParkingFacility --type json --file /mdpf.json --jsonArray && \
 mongoimport --host mongodb --db mydb --collection WasteContainers --type json --file /mdwc.json --jsonArray && \
 mongoimport --host mongodb --db mydb --collection house --type json --file /house.json --jsonArray && \
 mongoimport --host mongodb --db mydb --collection person --type json --file /person.json --jsonArray && \
 mongoimport --host mongodb --db mydb --collection truck --type json --file /truck.json --jsonArray && \
 mongoimport --host mongodb --db mydb --collection vehicle --type json --file /vehicle.json --jsonArray