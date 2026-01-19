# Hybrid-BGP-OSPF-Enterprise-Network-with-Dual-Path-Redundancy-Network-Design
Enterprise network using BGP primary path through transit providers with OSPF backup internally. Dual border routers connect client networks, providing redundancy and asymmetric routing between sites via protocol redistribution.

**Key Features**
1. Primary Path: BGP routing through transit providers (AS200 → AS300)
2. Backup Path: OSPF internal routing for redundancy
3. Automatic Failover: Seamless transition between protocols
4. Asymmetric Routing: Optimized path selection per traffic direction
5. Route Redistribution: Controlled exchange between protocols

**BGP Implementation**
1. AS100 and AS400 as edge autonomous systems
2. AS200 and AS300 as transit providers
3. Network statements for client prefix advertisement

**OSPF Implementation**
1. Single Area 0 for all OSPF routers
2. Client networks advertised internally
3. Administrative distance manipulation for protocol preference

![Alt text](https://github.com/rezaul1871/Hybrid-BGP-OSPF-Enterprise-Network-with-Dual-Path-Redundancy-Network-Design/blob/3250b35cb35e9103140aa33944122f077e25b487/Topology.png)

**Testing Methodology**
1. Verify BGP path connectivity as primary link
2. Test OSPF backup path functionality (by shutdown one interface)
3. Simulate link failures to validate failover
4. Monitor routing table convergence
5. Validate end-to-end application connectivity
