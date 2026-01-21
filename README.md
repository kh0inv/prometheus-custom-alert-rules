prometheus-rules/
├── infrastructure/              # The "Hardware" Layer
│   ├── node.rules.yaml          # CPU, Mem, Load
│   ├── filesystem.rules.yaml    # Disk usage, inodes
│   └── network.rules.yaml       # Dropped packets, bandwidth
├── platform/                    # The "Orchestration" Layer
│   ├── k8s-system.rules.yaml    # Kubelet, API Server
│   ├── k8s-resources.rules.yaml # PVCs, Pod stuck states
│   └── ingress.rules.yaml       # Nginx/Ingress controller stats
├── middleware/                  # The shared services, platform services
│   ├── redis.rules.yaml
│   ├── kafka.rules.yaml
│   └── postgres.rules.yaml
└── application/                 # The "Workload" Layer
    ├── common.rules.yaml        # Rules that apply to ALL apps (e.g., 500 error rate)
    ├── payment-service.yaml     # Specific business logic
    └── auth-service.yaml
