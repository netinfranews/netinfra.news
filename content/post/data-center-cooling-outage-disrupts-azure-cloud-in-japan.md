+++
date = "2017-03-31"
draft = false
title = "Data Center Cooling Outage Disrupts Azure Cloud in Japan"
author = "DrewT"
+++

A long list of Microsoft Azure cloud services malfunctioned for hours Friday for a subset of customers using services hosted in a Microsoft data center in Japan due to a cooling system outage that was caused by a failed RUPS (rotary uninterruptible power supply).

Customers had trouble connecting to resources that leverage storage infrastructure in the Japan East region, according to an update on the Azure status website. Both storage and virtual machines were impacted, along with many more cloud services, such as Web Apps, Backup, HDInsight, Key Vault, and Site Recovery. Issues included unavailability of virtual machines and VM reboots.

“Engineers have identified the underlying cause as loss of cooling which caused some resources to undergo an automated shutdown to avoid overheating and ensure data integrity and resilience,” the status page read as of noon Pacific Time. The data center is managed by a third-party vendor, not Microsoft.

The UPS system failure interrupted power supply to the power distribution system that feeds all air handling units of the data center hosting Japan East, shutting the air handlers down, an update posted later in the day said. “The result of the air handlers failing was continued increase in temperature within the entire data center.”

Technicians working for the third-party data center provider and Microsoft’s site services personnel restarted the air handlers and used outside airflow to cool the facility.

The issues started around 7 a.m. Pacific Time and continued into the afternoon as Azure engineers worked to restore the systems. Temperature in the facility was back within operational ranges around 9 a.m., and by 3 p.m. engineers confirmed the storage infrastructure and all dependent services had recovered successfully.

As of the morning of April 3, the company has not said what the cause of the UPS failure was. The latest update on the incident, posted on the day of the outage, said the root cause was still being investigated, and suspect components were sent for analysis.

Design of the cooling system and the power distribution system had typical redundancy built in for backup. The cooling system is N+1, meaning there is an extra cooling unit available in case one fails. The power distribution system was running at N+2, but one UPS in the parallel N+2 lineup failed and power was cut off to the entire cooling system in the data center.

While the most consequential cloud outage of the year so far – the Amazon Web Services storage service meltdown in late February – was caused by a mistyped command, Friday’s incident in Japan serves as a reminder of the extremely physical nature of the Cloud.

Cooling-related data center outages are common, but not nearly as common as electrical infrastructure problems, and the Microsoft outage is an example of a failure by the latter causing a failure of the former. Malfunctioning uninterruptible power supplies have consistently been reported as the most common cause of data center outages in regular surveys by the Ponemon Institute, commissioned by the company formerly known as Emerson Network Power (now known as Vertiv).

Microsoft Azure launched its Japan East region, hosted in a data center in the Saitama Prefecture, and its Japan West region, hosted in a data center in the Osaka Prefecture, in 2014.
