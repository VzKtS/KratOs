KratOs est une blockchain de gouvernance décentralisée construite entièrement from-scratch en Rust pur, sans dépendance à 
des frameworks blockchain externes.

Vision & Philosophie
"Protocole de coexistence, pas une application" - Un framework pour la coordination communautaire
Minimalisme & Auditabilité - Chaque ligne de code est visible et compréhensible
Durabilité long-terme - Conçu pour survivre des décennies
Architecture Technique
Couche	Composants
Types	15 modules (primitives, signatures, transactions, blocs, merkle, fraud proofs)
Contrats	13 contrats système (KRAT, staking, governance, sidechains, identity, arbitration)
Consensus	VRF-based Proof-of-Stake avec Validator Credits
Réseau	P2P via libp2p (gossipsub, mDNS, Kademlia)
Stockage	RocksDB
RPC	JSON-RPC via Warp
Structure des Fichiers
rust/kratos-core/src/
├── types/       # Types primitifs (15 modules)
├── contracts/   # Contrats système (13 modules)
├── consensus/   # Mécanisme PoS/VRF (11 modules)
├── network/     # P2P networking
├── node/        # Service node, mempool, producer
├── rpc/         # API JSON-RPC
├── storage/     # Backend RocksDB
└── tests/       # 560+ tests

Spécifications Implémentées (Phases 1-6 complètes)

SPEC v1: Validator Credits (dual-token: KRAT économique, VC gouvernance)
SPEC v2: Economics (émission décroissante 5%→0.5%, burn croissant 1%→3.5%)
SPEC v3.1: Sidechains hiérarchiques (L1 Root → L2 Host → L3 Community)
SPEC v4: Identité & Réputation
SPEC v5: Invariants de sécurité
SPEC v6: Meta-Gouvernance avec 5 axiomes constitutionnels
SPEC v7: Pouvoirs d'urgence avec circuit breakers
SPEC v8: Résilience long-terme & Forks (en cours ~40%)

Axiomes Constitutionnels (Immuables)

ExitAlwaysPossible - Sortie toujours possible sous 30 jours
NoRetroactivePunishment - Pas de punition rétroactive
IdentitySovereignty - Souveraineté de l'identité
TransparencyRequired - Transparence obligatoire
ForkingLegitimate - Le fork est toujours légitime

État Actuel

~53,500 lignes de Rust
560+ tests passants
Infrastructure principale opérationnelle en devnet
Prochaines étapes: testnet multi-nœuds, fork execution pipeline
Total Security Fixes: 38 corrections de sécurité implémentées dans le projet.

2026 1er trimestre audit public
