# Mission 8 Reflection: The Cloud Security Engineer

Completing this laboratory helped me understand the importance of protecting cloud servers from unauthorized network access. I learned that deploying an application is not enough because the server also needs proper security configurations.

A host-based firewall protects a server by controlling network traffic directly on the machine. Even if attackers bypass the physical network perimeter, the firewall provides another layer of protection by restricting connections according to configured rules. This demonstrates the importance of defense in depth.

Managing open network ports is important because every unnecessary exposed service can become a possible entry point for attackers. By reviewing listening ports and allowing only required connections, administrators can reduce the attack surface of a server. The Principle of Least Privilege also applies to network access because services should receive only the connectivity they need.

Leaving a database port such as MySQL port 3306 open to the public internet is dangerous because unauthorized users may attempt password attacks or exploit database vulnerabilities. A database should normally be accessible only to trusted applications and authorized administrators through protected networks.

This activity also changed how I think about server security. I realized that even a simple web application requires careful configuration and continuous monitoring. I also learned that checking whether an application responds locally is different from verifying that external network traffic is properly filtered.

My GitHub cloud computing portfolio is becoming a useful record of my laboratory work. With the addition of Mission 8, it can show my progress in cloud infrastructure, deployment, operations, and security, alongside my previous completed activities. Organizing the documentation and screenshots helps me review the commands and explain what I learned from each mission.

Overall, this laboratory improved my awareness of cloud security responsibilities and the importance of protecting services before making them publicly accessible.
