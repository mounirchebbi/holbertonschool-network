```mermaid
graph TD
    A[User's Browser] -->|Type URL| B[DNS Resolver]
    B -->|Resolves Domain to IP| C[google.com IP:443]
    C -->|Encrypted HTTPS Request| D[Firewall]
    D -->|Inspected & Allowed| E[Load Balancer]
    E -->|Forwards Request| F[Web Server]
    F -->|Delegates| G[Application Server]
    G -->|Queries| H[Database]
    H -->|Returns Data| G
    G -->|Generates Page| F
    F -->|Serves HTML Page| A
