# A Real Internet Voting Implementation

The debacle in Iowa has made me reflect on the full extent to which people 
in general simply do not get it. So, look here, we'll build a fucking voting 
system.

We're going to use public key encryption to secure (and anonymize) our votes 
and a block chain ledger (based on HyperLedger) to store and tally the results.

    HLF_VERSION=1.4.0
    docker pull hyperledger/fabric-peer:${HLF_VERSION}
    docker pull hyperledger/fabric-orderer:${HLF_VERSION}
    docker pull hyperledger/fabric-ca:${HLF_VERSION}
    docker pull hyperledger/fabric-ccenv:${HLF_VERSION}
    docker-compose up

Now we have a simple election quorum going, with results persisted in a fully
distributed blockchain. But, we aren't doing any voting yet so there aren't
any results. That's fair, I suppose. We're gonna have to write some code!
