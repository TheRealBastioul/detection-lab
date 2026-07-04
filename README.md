```mermaid
flowchart TD
    subgraph Net [<b>Network</b>10.0.2.0/24<br>]
        subgraph A[Virtual Machines]
            B(Victim PC<br><i>10.0.2.3</i><br>Windows Server 2019) --> | logs | C
            C[Monitor<br>Security Onion]
        end
        D(Attacker PC<br><i>10.0.2.15</i><br>Kali Linux) --> | attack traffic | B
        D-.->|packet capture | C
    end
```

vincent@dimensionbeyond.space
onion-admin
