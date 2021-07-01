# Release note 20.4.2

![Une image contenant dessin

Description g&#xE9;n&#xE9;r&#xE9;e automatiquement](.gitbook/assets/0.png)![](.gitbook/assets/1.jpeg)

Release Notes

Dimonoff \| SCMS

Version 20.4.2

Release Notes – Dimonoff \| SCMS 20.4.2

**Release Date:** 2021-05-07

**What’s New:**

N/A

**Improvements:**

* The default logout timeout has been upgraded to 20 minutes instead of 10 minutes.
* In the menu Configuration -Devices – Details, the “Street Lamp Identifier” field has been expanded so you can see all the characters, even if it is a very long identifier.
* In the Maps menu, the connectivity information was added in the exported file.
* \(DOO\) In the Reports – Energy Logs menu, energy reports created by SCMS report generator have improved interpolation from the raw data \(by device – detailed report type\) received from Wireless Smart Lighting Nodes with older firmware version.
* \(DOO\) In the Configuration- Devices and Maps menus, SCMS provides more feedback to users while using the Rescue mechanism.

**Bug Fixes:**

* In the Security – User logs menu, dates in the executed report were off by one day. It is no longer the case.
* In certain cases, there was a mismatch between the “ON” percentage shown in the Zone Statuses menu and what is really on the map \(Dashboard menu\).
* Sometimes, after turning off a node, the dimming level was not updated to “0”.
* In the Dashboard menu, the “Not Responding” devices count did not match the value displayed on devices aggregation pie chart on the map.
* In the Configuration- Devices and Gateways Statuses menus, when querying Gateway configurations, there was a MySQL bug that could occur. That was fixed.
* In the Reports – Energy Logs menu, there was a partitioning failure error for the energy consumption logs table in the database.
* In the Reports – Energy Logs menu, when there is a lot of data to report, the “By Hours By Day \(table\)” report query would timeout before getting the results. We optimized the way this report is generated and increased the timeout.
* In the Reports – Energy Logs menu, “By Device – Detailed” report execution always produced data for one more day than what was requested.
* In the Reports – Energy Logs and Inventory menus, when opening “Energy Logs” or “Inventory” reports tab, there was an interface bug which would display only titles of the elements in the right section.
* In Administration – Parameters Management menu, the green check mark would not show after saving. We added it back.
* In the menu Configuration- Zones-Building, after creating floors in a building, you had to reload the application to see the modification on the map.
* In the Reports – Energy Logs menu, when exporting a “By Hour By Day \(table\)” report, the file would come out empty.
* In the Reports – Energy Logs menu, “By Hour By Day \(chart\)” report had the wrong hours indexes, so energy value on the graph was assigned to the previous hour.
* In the Dashboard menu, when saving a searchable field using the hooked parameter on the device information panel, the corresponding value displayed in “Configurations – Devices – Parameters” was changed to something else.
* In the Security menu, we fixed the problem that made deleting a role impossible.
* In the Dashboard menu, when a node was selected within a zone and you clicked on a new zone in the dropdown list, the zone changed, but the details panel did not update accordingly.
* In Zone Statuses menu, the total of intelligent devices value used for “Alarms” and “Responding” percentage calculation was not the same than for the other fields.
* In the Reports – User-Defined queries, a User Defined Query that applied to a range of dates \(condition: between dates\) would not execute anymore.
* \(DOO\) – For H3 generation nodes, the “Restore Power On” alarm wasn’t mapped correctly so it appeared as “N/A” in the interface \(Dashboard menu\).
* \(DOO\) – In the Configuration – Devices – Parameters menu, the “Restore Power On” alarm was not configurable for H3 generation nodes.
* \(DOO\) – Remove N/A sometimes displayed in alarms for H3 generation nodes.
* \(TLMW\) – We added a mechanism to be able to synchronize modifications to more than one schedule at a time for Telematics nodes.
* \(TLMW\) – It was not possible to synchronize a Telematics gateway.

**Deprecated:**

N/A

**Known Limitations:**

* In the Dashboard menu, the number of displayed devices on the same business unit is 101k.

