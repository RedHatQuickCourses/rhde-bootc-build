For each of the following scenarios, which approach to deploying RHEL systems would be most adequate?
There could be more than one right answer.

Q1: A manager's workstation in a retail store, to run text processors, spreadsheets, email clients, and also access multiple corporate systems.

A: Traditional RHEL (with package mode)
Correct: This is a general-purpose workstation which likely runs a popular desktop operating system, such as Windows and MacOS.
<a href="https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux/workstations">RHEL for Workstations</a>, <a href="https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux/red-hat-enterprise-linux-for-developers">RHEL for Developers</a>, and the community supported <a href="https://fedoraproject.org">Fedora Linux</a> are also good choices for this kind of user workstation.

A: Red Hat Device Edge (with image mode)
Incorrect: Red Hat Device Edge is designed for special-purpose devices instead of general purpose workstations.
You CAN use image mode to provision graphical office workstations, most likely they require RHEL subscriptions instead of Red Hat Device Edge subscriptions.

Q2: A kiosk machine in a large department store, that enables customers to query the price and other information about a product, such as nutrients and potential allergens for food products, or warranty terms and technical specifications for electronics, using a barcode reader and a touch screen.

A: Traditional RHEL (with package mode)
Incorrect: Though kiosk machines have been frequently configured from standard desktop operating systems, they become high-maintenance and even potential sources of embarrassment if customers can get access to other applications on the device.
A lower maintenance approach, such as the one from image mode systems, fits this scenario better.

A: Red Hat Device Edge (with image mode)
Correct: This is an appliance-like device, which should be just turned on and be available to customers in different parts of the store, requiring minimal maintenance.

Q3: A database server, which stores inventory levels and regional prices of goods in a large retail store, among other data required by multiple client devices for different business processes that happen in the store itself.
A: Traditional RHEL (with package mode)

Correct: This is likely a server-class machine locked in a server room, and possibly a member of a high-availability (HA) cluster with other similar machines in the store.
Even if not HA it is likely managed by corporate IT like any other departmental server in branch offices.

A: Red Hat Device Edge (with image mode)
Incorrect: This server machine is probably too powerful for the Red Hat Device Edge subscription, but a small and single-purpose database server could be deployed and managed as an edge device.
You CAN provision and configure a large server using image mode for RHEL, but using a RHEL subscription instead of a Red Hat Device Edge subscription.

Q4: A controller for security access devices, such as card readers, face recognition cameras, fingerprint readers, and electronic locks in access doors, which connects either to the corporate identity management and human resources databases or to a local replica of that database on the building or campus.
A: Traditional RHEL (with package mode)
Incorrect: These computers are likely close to the security access devices, many of them are deployed in different parts of the building or campus, and they should be resistant to tampering, which makes them better suited for image mode deployments than to traditional package mode deployments.

A: Red Hat Device Edge (with image mode)
Correct: In addition to the considerations in the previous answer, these computers are likely rugged for outdoor conditions, and must be quickly replaceable in case of hardware failures.
Besides, they are likely provided as appliances by the security equipment vendor, instead of managed by corporate IT as other LOB servers.

Q5: An image recognition application, which monitors goods at different stages of an assembly line and flags defective ones, reducing the need for human inspection of samples from each batch of goods.

A: Traditional RHEL (with package mode)
Correct: Depending on the hardware requirements of its image recognition application, this might require entitlements from a Traditional RHEL subscription, but be deployed and managed using image mode technologies.
It could use compute device which is rugged for factory floor conditions and provides compute capacity similar to a data center server, as opposed to a leaner edge device, and may not meet the criteria for Red Hat Device Edge subscriptions.

A: Red Hat Device Edge (with image mode).
Correct: As a single-purpose appliance, this is better suited to be deployed and managed as an image mode system.
Be aware that, to be entitled using Red Hat Device Edge subscriptions, its image recognition application must fit edge systems with a single CPU core and reduced memory.
Some of those devices do offer GPUs and other kinds of hardware accelerators suitable for this kind of applications.
