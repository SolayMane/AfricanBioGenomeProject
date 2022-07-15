```mermaid
    graph TD
        dir(<img src='https://user-images.githubusercontent.com/22656460/176923736-04cf574b-806b-4c7a-8ff8-c1d218164ecc.png', width='120', heigth='100'/>) --> |HWM gDNA extraction| B(gDNA)

        B --> C(Short insert sizelibrary<br>sequencing data)
        B --> A(Short insert size/mate pair <br>libraries sequencing data)
        C -->|<b>Genome survey<br><i>Kmer analysis| D((<b>Genome Summary))
        A -->|Hierarchical shotgun strategy<br><i>SOAPdenovo| E((<b>Draft genome assembly))
        B--> |<img src='https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/10x_Genomics_logo.svg/1200px-10x_Genomics_logo.svg.png', width='50'/>|f(10X  Genomics<br> sequencing library)
   
        f --> E
        B --> |stLFR strategy <img src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdlH-w9OzaDVzsoH7LXJST3PdCwxQu33J9gDmu9Kd1XRmSFuFGkL5pKTBBIsdIc0q0Bts&usqp=CAU', width='70'/>| g(Single tube long<br> fragment reads sequencing)
        g --> E
        B --> |<i>strategy 4| e(3rd generation<br> long reads sequencing)
        e --> E
        D -->|Complex genomes, full-legth transcriptome| F((<b>Transcriptts<br> assembly))
        B--> |Hi-C library sequencing<br>data| G((<b>Chromosome<br>assembly))
        classDef green fill:#9f6,stroke:#333,stroke-width:2px
        classDef orange fill:#f96,stroke:#333,stroke-width:4px
        classDef blue fill:#9f2,stroke:#333,stroke-width:2px
        class B green
        class Q,A,g,f,C,e orange
        class D red
 ```
