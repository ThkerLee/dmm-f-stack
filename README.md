# 1.  Introduction:

# ![nStack_Architecture](resources/nStack_Architecture.png "nStack_Architecture")

DMM (Dual Mode, Multi-protocol, Multi-instance) is a framework between applications
and transport layer of networking stack. This framework can hosts different types of
networking stack instances operating on different domains (kernel/user-space) or even with
different protocol suites (TCP/IP, RDMA, or others). Application can use different type of
protocol stack implementations based on functional/performance requirements.


# 2.  History:
Emerging applications are bringing extremely high-performance requirements to the
network system. Eg. AR/VR, IOT etc. And Many of them coming with their unique demand
of QOS/SLA. Some application need low latency network, some need high reliability etc.
Though such performance targets should be required for the complete communication system,
the transport layer protocols play a key role and encountered a relatively higher
challenge, because traditionally the TCP-based transport layer exploits the “best-effort” principle
and provides no performance guarantees in its nature. However, as Internet applications rapidly
grow and diversify, an all-powerful or one-fits-all protocol or algorithm becomes less feasible.
Thus, the traditional single-instance TCP-based network stack bears great challenges when
serving many applications with different QoS/SLA requirements  simultaneously on the
same platform. Also Moving the networking stack out of the kernel is an obvious trend in both
the industry and literature. Technologies like DPDK, etc improving performance of network
stack, by bypassing the kernel, avoiding context-switching and data copies, as well as providing
a complete set of packet-processing acceleration libraries. Keeping above trends in mind the
DMM/nStack provides a framework where, system operators can plug in dedicated types of
networking stack instances according to performance and/or functional requirements from
the user space applications. Application doesn't have to worry about change their transport
layer API. A lightweight nStack management daemon is responsible for maintaining the stack
instances and the app/socket-to-stack-mappings, which are provided via the orchestration
/management interface. So DMM provide a framework which can hide all the complexity of
different transport layer protocol and also provide the flexibility to choose a protocol stack
from manybased on functional/performance requirements.


# 3.  Quick Start
Refer doc/Build_DMM.md 


# 5. More Information

- https://wiki.fd.io/view/DMM
- https://wiki.fd.io/view/Project_Proposals/DMM
- Enabling “Protocol Routing”: Revisiting Transport Layer Protocol Design in Internet
Communications(http://ieeexplore.ieee.org/document/8114687/)


