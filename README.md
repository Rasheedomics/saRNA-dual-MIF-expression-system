Phase 1 Construct Design Overview

This project presents the in-silico design of a self-amplifying RNA (saRNA) construct for dual antigen expression targeting parasite-derived macrophage migration inhibitory factors (MIFs) from Plasmodium and Leishmania.
The final construct follows the organization:
Replicon -> Subgenomic promoter -> PMIF -> Subgenomic promoter -> LmMIF -> Poly(A) tail
This design enables each antigen to be independently transcribed using subgenomic promoters, which would presumably result in equal expression.

2. Construct Architecture and Sequence Components

The construct was put together with the following DNA fragments:

Replicon backbone (vector)
	<img width="43" height="35" alt="image" src="https://github.com/user-attachments/assets/8868954e-5378-493d-aec1-37eb2fb1e498" />
Subgenomic promoter (SGp)- first cassette.
	<img width="43" height="35" alt="image" src="https://github.com/user-attachments/assets/c30eb2df-cbf3-4abb-ad0c-c91315e97882" />
PMIF coding sequence
  <img width="43" height="35" alt="image" src="https://github.com/user-attachments/assets/d3ab8cc6-1d21-4523-ac80-5e847e60a4dc" />
Subgenomic promoter (SGp) - second cassette.
  <img width="43" height="35" alt="image" src="https://github.com/user-attachments/assets/8a33d3a6-ea35-4ce3-b2a3-3418def87fcc" />
LmMIF coding sequence
  <img width="43" height="35" alt="image" src="https://github.com/user-attachments/assets/dfa09e39-f69a-4055-9cc4-4459506e0182" />
poly(A) tail

All the sequences were imported and curated in SnapGene, which is consistent across individual .dna files.

Strategies: Gibson Assembly (3) Cloning Strategy. The construct was simulated in-silico by coupling in SnapGene with Gibson Assembly-based strategy.

Key principles:
The fragments are attached through overlapping homologous regions (~20 bp).
The sequences were coupled with in-silico PCR using primers that contained overlapping sequence.
Direct insertion of non-coding elements (SG promoter, polyA) was done.

4. Fragment Arrangement in SnapGene.
Vector
A placeholder Alphavirus replicon sequence was used as a linearized vector.
Downstream insertions of replicase region.

Fragment Setup
Fragment		Component			            Strategy
1.         	SG promoter			          Used directly as fragment
2.			    PMIF				              PCR amplification
3. 			    SG promoter (copy)		    Used directly as fragment
4.			    LinfMIF			            	PCR amplification
5.			    poly(A) tail		        	Used directly as fragment


Primer sequences were developed in a way that the 5’ ends of each forward primer have an overlap sequence that is homologous to the next downstream fragment with the 3’ ends annealing to the template DNA. This design uses a forward primer in the downstream fragment that contains the sequence overlap with the second subgenomic promoter to allow assembling. Equally, the reverse primers were designed to have an overlap to the next fragment, which contains the poly(A) tail, and thus, allows assembly across fragment junctions when using Gibson Assembly.
Caution: The poly(A) overlap is simplified to allow in-silico design and would need to be refined to allow experimental implementation.

6. Assembly Outcome

The fragments were arranged and positioned in the following order in SnapGene:

Replicon -> SGp1 -> PMIF -> SGp 2-> LmMIF -> polyA

Result: SnapGene was not able to complete automatic assembly because of the poor overlap resolution, but the following were obtained:
      Complete fragment organization
      Coding sequence PCR primer design.
      Rational assembly architecture that is compatible with saRNA systems.
      
7. Technical Considerations
Primer specificity was restricted by repetitive sequences of placeholders (e.g., SG promoter).
The definition of the overlap regions was done manually and would require optimization.

9. Conclusion
The entire in-silico cloning plan of a dual-antigen saRNA construct was created in SnapGene.
This workflow demonstrates:
    Rational construct design
    Gibson assembly planning
    PCR-based fragment generation integration.

The construct is prepared for:
Overlap refinement, downstream structural and immunological validation with real sequences in places of placeholders.

## References
1. Blakney AK, Ip S, Geall AJ. An update on self-amplifying mRNA vaccine development. Vaccines (Basel). 2021;9(2):97.
2. Chang C et al. Self-amplifying mRNA bicistronic influenza vaccines raise cross-reactive immune responses in mice and prevent infection in ferrets. Mol Ther Methods Clin Dev. 2022;27:195–205.
3. Frolov I et al. Alphavirus-based expression vectors: Strategies and applications. Proc Natl Acad Sci USA. 1996;93(21):11371–11377.


##Author
Abdulrasheed Buhari
