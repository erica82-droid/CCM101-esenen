# Mission Reflection  Cloud Security Engineer

Completing this cloud security mission helped me understand the importance of protecting servers through proper firewall configuration and network security practices.

A host-based firewall protects a server by controlling incoming and outgoing network traffic directly on the machine. Even if an attacker bypasses the physical network perimeter, the host-based firewall can still block unauthorized connections based on its configured rules. This provides an additional layer of defense and helps prevent attackers from accessing services that are not intended to be publicly available.

Managing open network ports is critical because every open port can potentially provide an entry point for attackers. Unnecessary ports may expose vulnerable applications or services that could be exploited to gain unauthorized access. By following the Default Deny principle and allowing only the ports required for legitimate services, administrators can reduce the server's attack surface and improve its overall security.

In a real enterprise environment, leaving a database port such as 3306 for MySQL open to the public internet is dangerous because attackers could attempt password guessing, exploit database vulnerabilities, or access sensitive information if authentication or configuration is weak. Database services should generally be restricted to trusted application servers and authorized administrators rather than exposed to everyone on the internet.

This mission changed my perspective by showing me that a server can become vulnerable through simple configuration mistakes, such as leaving unnecessary ports open or enabling a firewall without first allowing SSH. I learned that security requires careful planning, testing, and continuous verification rather than simply installing security tools.

With eight completed missions, my GitHub portfolio represents my growing knowledge of cybersecurity, system administration, and technical documentation. It also demonstrates my ability to follow instructions, execute commands, troubleshoot errors, and document my work. I recognize that a portfolio is more valuable when it contains verified results and clear explanations of what I learned. Moving forward, I want to continue improving my practical skills, documenting my projects accurately, and applying security best practices to real-world systems.
