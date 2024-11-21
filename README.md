# Graph Neural Network for Molecule Property Prediction

This project explores the use of Graph Neural Networks (GNNs) to predict molecular properties, such as solubility, leveraging the ESOL dataset from MoleculeNet. The aim is to investigate the predictive power of GNNs and the clustering of molecular embeddings to identify groups with different predictability levels.

---

## Highlights of the Project

### Dataset
- **Source**: MoleculeNet ESOL dataset.
- **Key Features**: 
  - 1128 molecules with detailed graph structures.
  - Node features representing molecular properties.
  - Target variable focused on solubility prediction.

### Modeling Approaches
1. **Regularized GCN**:
   - Employs dropout, batch normalization, and pooling mechanisms to improve generalization.
   - Captures complex relationships between molecular nodes and edges.

2. **Overfitting GCN**:
   - A deliberate overfitting approach to identify subsets of easily predictable molecules.
   - Helps uncover inherent clusters of molecules based on their predictability.

3. **Clustering-Based Analysis**:
   - Extracts GNN embeddings and applies clustering algorithms (KMeans, DBSCAN).
   - Identifies groups with similar molecular behavior and predictability.
   - Focused refinement on the largest cluster of "easy-to-predict" molecules.

---

## Results

- The **Regularized GCN** provided robust performance, balancing training and testing losses effectively.
- The **Overfitting GCN** revealed clusters of molecules, highlighting inherent structural or property-based grouping.
- Clustering analysis identified a prominent cluster with high predictability. Further fine-tuning on this cluster led to significant accuracy improvements.

### Final Model Performance:
- **Training Loss**: ~0.468
- **Testing Loss**: ~0.463

---

## Insights and Future Directions

- **Predictability Clusters**: Molecules can be grouped based on their predictability, opening avenues for specialized models for specific clusters.
- **Advanced GNN Architectures**: Future exploration of GNN variants (e.g., Graph Attention Networks, GraphSAGE) could enhance performance further.
- **Generalization Across Datasets**: Applying the framework to other molecular datasets can validate its effectiveness and generalizability.

---

## Acknowledgements

Special thanks to:
- **PyTorch Geometric**: For its powerful graph processing tools.
- **MoleculeNet**: For providing curated datasets for machine learning research.
- **RDKit**: For its molecular visualization and processing capabilities.

This project is a step forward in understanding molecular properties using graph-based deep learning techniques.
