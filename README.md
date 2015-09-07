# SHIELD

This project aims to provide a solution to specific problems.

## Activity : data collection

NGO activists set up a data collection zone, and invites the population to give them informations.
Informations are recorded on digital media. Those media are sent back to the NGO headquarters for analysis.

These informations may be very sensitive, and put people that expressed them in danger of violent repression.

Thus, anonymity and deniablility should be in our objectives.

## Threat model

Some states may not desire the expression of uncontrolled informations discussing issues inside their land.
Armed forces may operate an intervention in the data collection zone in order to destroy or collect the informations recorded.

Military RF interception material may be used to record the RF activity in the collection zone.

## Proposed solution

We will try to build a safe data collection tool.

Each mission needs to be prepared in a safe environment, with a predefined list of the hardware that will be used.
In this safe environment (NGO headquarter), the encryption keys will be generated, and decryption keys will be kept safe.
The list of involved hardware will be used in the configuration of the system built for the mission.

A central station will provide a Wi-Fi network to registered known stations.
The Wi-Fi network security will be WPA2. The usage of a PSK vs EAP will be decided later.

The central station will provide a DHCP and DNS local environment.
The central station will provide a web application.

The client stations used in data collection will use a standard embedded web browser to access the central web application.
No data will be kept on the client stations (no cache, etc.)

The central station operating system will be an open source free operating system (e.g. debian) running on an encrypted filesystem.
The central station encrypted filesystem key will be stored on an easily destroyable external media (e.g. /boot/ on a SD card).

An emergency cryptoprotection procedure should be defined.
This procedure should destroy (shred) the keys and power off the central station, leaving an unusable cryptobricked filesystem.
Hopefully, the NGO headquartes would still be able to decrypt the filesystem and recover the data.

Activation of the cryptoprotection procedure should be possible via logical and physical ways :
 - via a functionality of the web application (red button), triggering emergency procedures operated autonomously by the central station (delete keys, power off).
 - via manual unplugging of the power source of the central station, and manual destruction of the key storage media



Feel free to discuss these propositions.
