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
    docker-compose -f test/fixtures/docker-compose-2orgs-4peers-tls.yaml up
