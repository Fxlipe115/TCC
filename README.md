# A Hybrid Multi-Authority Attribute-Based Encryption Scheme For Securing HIoT Data

**Undergraduate Thesis in Computer Science**  
**Universidade Federal do Rio Grande do Sul (UFRGS)**  
**Instituto de Informática**

**Author:** Felipe de Almeida Graeff  
**Advisor:** Prof. Dr. Jéferson Campos Nobre  
**Co-advisor:** M.Sc. Laura Rodrigues Soares  

**Defended:** July 8, 2025  
**Grade:** A  
**Status:** ✅ **Completed and Approved**

### Examination Committee

**President:** Prof. Dr. Jéferson Campos Nobre  
**Members:**
- Prof. Dr. Eder John Scheid  
- Prof. Dr. Weverton Luis da Costa Cordeiro

---

## Abstract

The proliferation of Health Internet of Things (HIoT) devices has created an urgent need for secure and decentralized data sharing mechanisms that protect sensitive patient information while enabling flexible access for multiple stakeholders. Existing decentralized storage architectures for HIoT, specially the ones using blockchain, often lack a concrete cryptographic layer that provides fine-grained access control, leaving data vulnerable to unauthorized access. 

This thesis addresses this gap by proposing, implementing, and evaluating a hybrid cryptographic scheme that combines Multi-Authority Attribute-Based Encryption (MA-ABE) with symmetric Advanced Encryption Standard (AES) encryption to secure HIoT data. The proposed solution leverages the MaabeRW15 scheme to allow access policies to be defined over attributes distributed across multiple independent authorities, while efficient AES encryption is used for large data payloads. 

A comprehensive performance evaluation of a proof-of-concept implementation was conducted to measure the system's scalability and computational overhead. The results demonstrate that the hybrid approach is efficient for securing large datasets and that system performance scales effectively with process-based concurrency, though it is sensitive to the complexity of access policies and high user loads. This work confirms the viability of the proposed scheme as a practical method for enforcing robust, fine-grained access control in decentralized HIoT data management systems, offering a significant enhancement to data privacy and security.

## Key Contributions

1. **Hybrid Cryptographic Framework**: Design and implementation of a novel hybrid system combining MA-ABE with AES encryption for HIoT data security
2. **Performance Analysis**: Comprehensive evaluation of system scalability and computational overhead across multiple dimensions
3. **Practical Implementation**: Development of a proof-of-concept API with complete encryption/decryption workflows
4. **Security Enhancement**: Addressing the cryptographic gap in existing decentralized HIoT storage architectures

## Keywords

- **MA-ABE** (Multi-Authority Attribute-Based Encryption)
- **Hybrid Cryptography**
- **Access Control**
- **HIoT** (Health Internet of Things)
- **Data Security**
- **Performance Analysis**
- **Decentralized Systems**

## Repository Structure

```
├── main.tex                 # Main thesis document
├── preamble.sty            # LaTeX preamble and styling
├── draftenvironment.sty    # Draft environment setup
├── revisornotes.sty        # Revision notes styling
├── biblio.bib              # Bibliography file
├── dedicatory.tex          # Dedication page
├── epigraph.tex           # Epigraph page
├── images/                 # Figures and diagrams
│   ├── diagrams/          # System architecture diagrams
│   ├── phase1/            # Phase 1 performance results
│   ├── phase2/            # Phase 2 performance results
│   ├── phase3/            # Phase 3 performance results
│   ├── phase4/            # Phase 4 performance results
│   ├── key_size_analysis/ # Key size analysis results
│   └── size_analysis/     # Payload size analysis
├── inputs/                 # LaTeX class files and templates
└── README.md              # This file
```

## Technical Implementation

The implementation consists of:

- **Cryptographic Core**: MA-ABE scheme using MaabeRW15 algorithm
- **Symmetric Encryption**: AES for efficient payload encryption
- **API Framework**: RESTful API built with Flask and Flask-RESTX
- **Performance Testing**: Load testing with Locust framework
- **Concurrency**: Multi-process architecture using Gunicorn
- **Data Storage**: Redis for key management and persistence

### Key Technologies

- **Python 3.10** - Primary implementation language
- **Charm-Crypto** - Pairing-based cryptography library
- **Flask/Flask-RESTX** - Web framework and API development
- **Gunicorn** - WSGI server for production deployment
- **Redis** - In-memory data store for key management
- **Locust** - Load testing framework
- **Docker** - Containerization and deployment

## Performance Results

The evaluation demonstrated:

- **Scalability**: Effective scaling with process-based concurrency (25 workers optimal)
- **Efficiency**: Hybrid approach suitable for large datasets
- **Thread Sensitivity**: Limited benefit from thread-level concurrency due to Python's GIL
- **Policy Complexity**: Performance sensitive to access policy complexity and user load

## Academic Context

This work extends the decentralized storage framework proposed by Laura Rodrigues Soares (co-advisor) by implementing the cryptographic layer that was identified as future work in the original proposal. The thesis contributes to the field of secure healthcare data management by providing a practical solution for fine-grained access control in decentralized HIoT systems.

## Implementation Availability

The complete implementation source code is available at:
- **GitHub Repository:** https://github.com/Fxlipe115/ma-abe-flask
- **Archived Version:** https://doi.org/10.5281/zenodo.15741866

## University Information

**Universidade Federal do Rio Grande do Sul**
- **Rector:** Prof. Marcia Cristina Bernardes Barbosa
- **Vice-Rector:** Prof. Pedro de Almeida Costa
- **Dean of Undergraduate Studies:** Prof. Nádya Pesce da Silveira
- **Director of the Institute of Informatics:** Prof. Luciano Paschoal Gaspary
- **Coordinator of the Computer Science Program:** Prof. Álvaro Freitas Moreira
- **Head Librarian of the Institute of Informatics:** Alexsander Borges Ribeiro

## Build Instructions

This thesis was written using the UFRGS Informatics Institute LaTeX template available at: https://github.com/schnorr/infufrgs

To compile the thesis document:

```bash
# Using latexmk (recommended)
latexmk -pdf main.tex

# Or using pdflatex directly
pdflatex main.tex
bibtex main.aux
pdflatex main.tex
pdflatex main.tex
```

## License

This work is licensed under standard academic terms. The thesis document and associated materials are available for academic and research purposes. Please cite appropriately if using this work in your research.

## Citation

```bibtex
@mastersthesis{graeff2025hybrid,
  author = {Felipe Graeff},
  title = {A Hybrid Multi-Authority Attribute-Based Encryption Scheme For Securing HIoT Data},
  school = {Universidade Federal do Rio Grande do Sul},
  year = {2025},
  address = {Porto Alegre, RS, Brazil},
  month = {July},
  type = {Undergraduate Thesis in Computer Science},
  url = {[URL will be available in LUME repository]},
  type={Bachelor's Thesis}
}
```

The complete thesis document will be made publicly available through the UFRGS thesis repository.

---

**Final Version** - Repository archived on July 17, 2025  
**Defense Date:** July 8, 2025  
**Status:** Completed and Approved ✅

*This repository contains the complete final version of the undergraduate thesis as submitted and approved by the examining committee.*
