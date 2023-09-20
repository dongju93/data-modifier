# Raw log
## Target N-TAS Event
    ⊙ HttpThreat
        - 2023-06-05T05:31:57.691
        - 18572
        - {145e89fa-a02a-64d1-ff6e-000000000f00}
        - C:\\Program Files (x86)\\ESTsoft\\ALPDF\\ALPDF.exe
    ⊙ DnsCovertChannel
        - 2023-06-05T05:28:57.594
        - 11220
        - {145e89fa-894a-64d1-066a-000000000f00}
        - C:\\Program Files (x86)\\G2BRUN\\g2brun.exe

## Target E-TAS Event
    ⊙ HttpThreat
        - networkConnection ✅
        - processCreate ✅
        - imageLoad ✅
        - fileCreate ✅
        - fileDelete ✅
        
    ⊙ dnsQuery
        - networkConnection ✅
        - dnsQuery ✅
        - processCreate ✅
        - imageLoad ✅
        - registryValueSet ✅

### Target E-TAS Candidate
    ⊙ networkConnection
        - Network
        - Event 3
    ⊙ dnsQuery
        - Network
        - Event 22
    ⊙ processCreate
        - Process
        - Event 1
    ⊙ imageLoad
        - File
        - Event 7
    ⊙ fileCreate
        - File
        - Event 11
    ⊙ registryValueSet
        - Registry
        - Event 13
    ⊙ fileDelete
        - File
        - Event 23
<br/><br/><br/>


# Detect log
## Goal
    단일 Device 에서 특정한 기간(약 한달) 동안
    N-TAS 탐지이벤트와 E-TAS 탐지이벤트가 모두 검출이 되는 상황
## Target
    ⊙ Datetime
        - 2023.07.01 ~ 2023.07.30 ✅
        - Random datetime ✅
    ⊙ Counts
        - 300 ✅
## Common spec
    ⊙ N-TAS 기준
        - srcAddr : 41.179.253.229 ✅
    ⊙ E-TAS 기준
        - agentName : DESKTOP-0FS3LG3 ✅
        - agentId : f98ce9dc-4df6-445a-890d-c7a5368c230d ✅
## N-TAS log
    ⊙ Target detect event
        - HttpThreat ✅
        - DnsCovertChannel ✅
## E-TAS log
    ⊙ Target detect event
        - Randsomware ✅
        - Rootkit ✅
        - Bootkit ✅


<br/><br/>



#### Copyright 2023. ClumL Inc. all rights reserved