---
author: "Alyssa Müller (Alyssa-11), Francine Diethelm (fanarctica), Anais Prado (anais.prado), Max Condouret (madmax136)"
---

Task a)

Title: Long-read RNA sequencing

Intro: Short-read-sequencing works by fragmenting the transcripts into small sequences of a maximal length of a few hundred base pairs. Allowing for a high-throughput and accuracy, but making it hard to infer connections between different RNA isoforms and recreating the full-length transcript. Long-read-sequencing allows for full-length sequencing of RNA molecules. There are two main technologies used for long-read-RNA sequencing: Pacific Biosciences (PacBio)  and Oxford Nanopore Technologies (ONT).

PacBio Method: First of all, an RNA strand is isolated and reverse transcripted into complementary DNA (cDNA). The double stranded cDNA is then ligated at each side with SMRTbell adapters that are hairpin shaped and this transforms the cDNA into a circular template, which is called a SMRTbell library. The library is then immobilized in a specific well of a SMRT cell called a zero-mode waveguide (ZMW). Each ZMW contains a DNA Polymerase which binds to the SMRTbell adapter and then reads and transcribes the two complementary strands. When a nucleotide is being held in the Polymerase’s active site for complementarity check, a laser is being pointed at the nucleotide in a precise way (for clean signal). Since each nucleotide (A,C,G,T) contains a unique fluorescent dye attached to its corresponding phosphate terminal, they absorb and reflect the laser light differently which can be captured by sensors. The duration of the pulse will also tell us if there is complementarity. Indeed, if the pulse is long the nucleotide was transcripted, if the pulse was short the nucleotide was not complementary to the strand’s nucleotide.
Since the Library is circular, this allows for multiple subreads which in turn offers excellent precision (99.9%). This is because the subreads can be collapsed into a high consensus read. In particular, each subread contains random errors (about 10-15%) but all subreads are then aligned and for each nucleotide it can be determined probabilistically what the correct read should be.

ONT Method: This method uses an array of nanopores, which are tiny holes, each connected to an electrode, measuring the electrical current flowing through the pores. When the cDNA molecules pass through the pores, the electrical current changes, depending on which base is currently passing through the pore. A base-calling algorithm analyses the disruption to the current and identifies the base, allowing for real-time sequencing.

References:
- ChatGPT prompt: “Explain how RNA PacBio sequencing works”
- ChatGPT prompt: “How exactly is the strand sequenced during the Polymerase transcription. Why is light emitted? How is it absorbed? Explain fluorescence in this context.”
- “PacBio Sequencing – How it Works”: https://www.youtube.com/watch?v=_lD8JyAbwEo
- Long-read RNA sequencing: A transformative technology for exploring transcriptome complexity in human diseases, Ament et al.