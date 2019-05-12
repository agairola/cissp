Disaster recovery planning (DRP) is the technical complement to the business-focused BCP exercise. It includes the technical controls that prevent disruptions and facilitate the restoration of service as quickly as possible after a disruption occurs.

## The Nature of Disaster

A disaster recovery plan should be set up so that it can almost run on `autopilot`. The DRP should also be designed to `reduce decision-making` activities during a disaster as much as possible. Essential personnel should be `well trained` in their duties and responsibilities in the wake of a disaster and also know the steps they need to take to get the organization up and running as soon as possible. We’ll begin by analyzing some of the possible disasters that might strike your organization and the particular threats that they pose.

### Natural Disaster

A disaster recovery plan should provide mechanisms for responding to both types of disasters, either with a gradual buildup of response forces or as an immediate reaction to a rapidly emerging crisis.

> Note: Ensure that your organization has sufficient insurance in place to protect it from the financial impact of a flood under FEMA’s National Flood Insurance Program.

#### Earthquakes

  * More likely to occur along known fault lines that exist in many areas of the world. A well-known example is the San Andreas Fault (Wester US).

  * If you live in a region along a fault line where earthquakes are likely, your DRP should address the procedures your business will implement should a seismic event interrupt your normal activities.

#### Floods

  * Some flooding results from the `gradual accumulation` of rainwater in rivers, lakes, and other bodies of water that then overflow their banks and flood the community. Other floods, known as `flash floods`, strike when a sudden severe storm dumps more rainwater on an area than the ground can absorb in a short period of time. Floods can also occur when `dams are breached`. Large waves caused by seismic activity, or `tsunamis`, combine the awesome power and weight of water with flooding, as we saw during the 2011 tsunami in Japan ([Fukushima](http://www.world-nuclear.org/information-library/safety-and-security/safety-of-plants/fukushima-accident.aspx)).

#### Storms

  * `Prolonged` periods of intense `rainfall` bring the risk of `flash flooding` described in the previous section. `Hurricanes and tornadoes` come with the threat of winds exceeding 100 miles per hour that undermine the structural integrity of buildings and turn everyday objects such as trees, lawn furniture, and even vehicles into deadly missiles. `Hailstorms` bring a rapid onslaught of destructive ice chunks falling from the sky. Many storms also bring the `risk of lightning`, which can cause severe damage to `sensitive electronic component`s. For this reason, your business continuity plan should detail appropriate mechanisms to `protect against lightning-induced damage`, and your disaster recovery plan should include adequate `provisions for power outages and equipment damage that might result from a lightning strike`. 

  > National Weather Service’s [National Hurricane Center](https://www.nhc.noaa.gov/)

#### Fires

  * Fires can start for a variety of reasons, both natural and man-made, but both forms can be equally devastating. During the BCP/DRP process, you should evaluate the risk of fire and implement at least basic measures to mitigate that risk and prepare the business for recovery from a catastrophic fire in a critical facility.

  > National Interagency Fire Center posts daily fire updates and forecasts on its [website](https://www.nifc.gov/fireInfo/nfn.htm)

#### Other Regional Events

  * Some regions of the world are prone to localized types of natural disasters. During the BCP/DRP process, your assessment team should analyze all of your organization’s operating locations and gauge the impact that such events might have on your business. For example, many parts of the world are subject to `volcanic eruptions`.

### Man-Made Disasters

#### Fires

  * Many smaller-scale fires result from human action—be it carelessness, faulty electrical wiring, improper fire protection practices, or other reasons

#### Acts of Terrorism

  * Since the terrorist attacks on September 11, 2001, businesses are increasingly concerned about risks posed by terrorist threats. These attacks caused many small businesses to fail because they did not have business continuity/disaster recovery plans in place that were adequate to ensure their continued viability. Many larger businesses experienced significant losses that caused severe long-term damage. 

#### Bombings/Explosions

  * Explosions can result from a variety of man-made occurrences. Explosive gases from leaks might fill a room/building and later ignite and cause a damaging blast. In many areas, bombings are also cause for concern. From a disaster planning perspective, the effects of bombings and explosions are like those caused by a large-scale fire. However, planning to avoid the impact of a bombing is much more difficult and relies on physical security measures 

#### Power Outages

  * Even the most basic disaster recovery plan contains provisions to deal with the threat of a short power outage. Critical business systems are often protected by uninterruptible power supply (UPS) devices to keep them running at least long enough to shut down or long enough to get emergency generators up and working. 

  > Check your UPSs regularly

  * Your BCP/DRP team should consider provisioning alternative power sources that can run business systems indefinitely. An adequate backup generator could make a huge difference when the survival of your business is at stake.

#### Network, Utility, and Infrastructure Failures
  
  *  Many businesses depend on one or more of these infrastructure elements to move people or materials. Their failure can paralyze your business’s ability to continue functioning.

  * You must also think about your internet connectivity as a utility service. Do you have sufficient redundancy in your connectivity options to survive or recover quickly from a disaster? If you have redundant providers, do they have any single points of failure?

#### Hardware/Software Failures

  * Like it or not, computer systems fail. Hardware components simply wear out and refuse to continue performing, or they suffer physical damage. Software systems contain bugs or fall prey to improper or unexpected inputs. For this reason, BCP/DRP teams must provide adequate redundancy in their systems. If zero downtime is a mandatory requirement, the best solution is to use fully redundant failover servers in separate locations attached to separate communications links and infrastructures (also designed to operate in a failover mode). 

  > Lessons learned during this blackout ( NYC BLACKOUT ) offer insight for BCP/DRP teams around the world and include the following:
  * Ensure that alternate processing sites are far enough away from your main site that they are unlikely to be affected by the same disaster.
  * Remember that threats to your organization are both internal and external. Your next disaster may come from a terrorist attack, a building fire, or malicious code running loose on your network. Take steps to ensure that your alternate sites are segregated from the main facility to protect against all of these threats.
  * Disasters don’t usually come with advance warning. If real-time operations are critical to your organization, be sure that your backup sites are ready to assume primary status at a moment’s notice.

#### Strikes/Picketing
 
  * Don’t forget about the importance of the human factor in emergency planning. One form of man-made disaster that is often overlooked is the possibility of a strike or other labor crisis.

#### Theft/Vandalism
 
  * Earlier, we talked about the threat that terrorist activities pose to an organization. Theft and vandalism represent the same kind of threat on a much smaller scale. In most cases, however, there’s a far greater chance that your organization will be affected by theft or vandalism than by a terrorist attack.

  > Keep the impact that theft may have on your operations in mind when planning your parts inventory. It’s a good idea to keep extra inventory of items with a high pilferage rate, such as random-access memory (RAM) chips and laptops. It’s also a good idea to keep such materials in secure storage and to require employees to sign such items out whenever they are used.

## Understand System Resilience and Fault Tolerance

Technical controls that add to system resilience and fault tolerance directly affect `availability`, one of the core goals of the CIA security triad (confidentiality, integrity, and availability). 

A *single point of failure (SPOF)* is any component that can cause an entire system to fail. If a computer has data on a single disk, failure of the disk can cause the computer to fail, so the disk is a single point of failure. 

*Fault tolerance* is the ability of a system to suffer a fault but continue to operate. Fault tolerance is achieved by adding redundant components such as additional disks within a redundant array of inexpensive disks (RAID) array, or additional servers within a failover clustered configuration.

*System resilience* refers to the ability of a system to maintain an acceptable level of service during an adverse event. This could be a hardware fault managed by fault-tolerant components, or it could be an attack managed by other controls such as effective intrusion detection and prevention systems.

> For example, if a primary server in a failover cluster fails, `fault tolerance` ensures that the system fails over to another server. `System resilience` implies that the cluster can fail back to the original server after the original server is repaired.

### Protecting Hard Drives

A common way that fault tolerance and system resilience is added for computers is with a RAID array. 

> Redundant Array of Inexpensive Disks (RAID) 

**RAID-0** This is also called striping. It uses two or more disks and improves the disk subsystem performance, but it does not provide fault tolerance.

**RAID-1** This is also called mirroring. It uses two disks, which both hold the same data. If one disk fails, the other disk includes the data so a system can continue to operate after a single disk fails.

**RAID-5** This is also called striping with parity. It uses three or more disks with the equivalent of one disk holding parity information. If any single disk fails, the RAID array will continue to operate, though it will be slower.

**RAID-10** This is also known as RAID 1 + 0 or a stripe of mirrors, and is configured as two or more mirrors (RAID-1) configured in a striped (RAID-0) configuration. It uses at least four disks but can support more as long as an even number of disks are added. It will continue to operate even if multiple disks fail, as long as at least one drive in each mirror continues to function.

Software-based RAID is inexpensive to implement, but can reduce overall system performance.
