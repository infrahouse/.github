# InfraHouse

**Simplifying Cloud Complexity**

[![Website](https://img.shields.io/badge/website-infrahouse.com-blue?logo=google-chrome)](https://infrahouse.com)
[![Terraform Registry](https://img.shields.io/badge/terraform-registry-623CE4?logo=terraform)](https://registry.terraform.io/namespaces/infrahouse)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-infrahouse--inc-0077B5?logo=linkedin)](https://www.linkedin.com/company/infrahouse-inc/)
[![Documentation](https://img.shields.io/badge/docs-infrahouse.com/docs-blue)](https://infrahouse.com/docs)

## About

InfraHouse provides **production-ready Terraform modules** for AWS infrastructure. Our modules are battle-tested, well-documented, and designed for startups that need enterprise-grade infrastructure without enterprise-grade complexity.

Founded by [Aleks Kuzminskyi](https://github.com/akuzminsky), who has built infrastructure for companies like Box, Dropbox, and Pinterest, InfraHouse delivers the same quality of infrastructure solutions to startups at a fraction of the cost.

## 🚀 Quick Start

Browse our modules on the [Terraform Registry](https://registry.terraform.io/namespaces/infrahouse) or explore the repositories below.
```hcl
module "openvpn" {
  source  = "infrahouse/openvpn/aws"
  version = "~> 0.2"
  
  backend_subnet_ids = module.network.subnet_private_ids
  lb_subnet_ids      = module.network.subnet_public_ids
  zone_id            = data.aws_route53_zone.main.zone_id
}
```

## 📦 Featured Modules

| Module | Description | Registry |
|--------|-------------|----------|
| [terraform-aws-openvpn](https://github.com/infrahouse/terraform-aws-openvpn) | OpenVPN server with Google OAuth portal | [![Registry](https://img.shields.io/badge/registry-latest-623CE4?logo=terraform)](https://registry.terraform.io/modules/infrahouse/openvpn/aws/latest) |
| [terraform-aws-secret](https://github.com/infrahouse/terraform-aws-secret) | Secrets with owner/writer/reader IAM roles | [![Registry](https://img.shields.io/badge/registry-latest-623CE4?logo=terraform)](https://registry.terraform.io/modules/infrahouse/secret/aws/latest) |
| [terraform-aws-ecs](https://github.com/infrahouse/terraform-aws-ecs) | ECS service with ALB, autoscaling, and monitoring | [![Registry](https://img.shields.io/badge/registry-latest-623CE4?logo=terraform)](https://registry.terraform.io/modules/infrahouse/ecs/aws/latest) |
| [terraform-aws-elasticsearch](https://github.com/infrahouse/terraform-aws-elasticsearch) | Self-managed Elasticsearch cluster | [![Registry](https://img.shields.io/badge/registry-latest-623CE4?logo=terraform)](https://registry.terraform.io/modules/infrahouse/elasticsearch/aws/latest) |
| [terraform-aws-debian-repo](https://github.com/infrahouse/terraform-aws-debian-repo) | Debian APT repository backed by S3 + CloudFront | [![Registry](https://img.shields.io/badge/registry-latest-623CE4?logo=terraform)](https://registry.terraform.io/modules/infrahouse/debian-repo/aws/latest) |
| [terraform-aws-state-bucket](https://github.com/infrahouse/terraform-aws-state-bucket) | S3 bucket + DynamoDB for Terraform state | [![Registry](https://img.shields.io/badge/registry-latest-623CE4?logo=terraform)](https://registry.terraform.io/modules/infrahouse/state-bucket/aws/latest) |

**[View all 45+ modules →](https://github.com/orgs/infrahouse/repositories?q=terraform-aws&type=all)**

## 🛠️ InfraHouse Toolkit

The [infrahouse-toolkit](https://github.com/infrahouse/infrahouse-toolkit) is a Python package providing CLI tools for infrastructure management:

- **ih-plan** — Summarize and publish Terraform plans to pull requests
- **ih-puppet** — Masterless Puppet runner for EC2 provisioning
- **ih-s3-reprepro** — Manage Debian repositories in S3
- **ih-elastic** — Elasticsearch cluster management
- **ih-github** — Manage GitHub Actions self-hosted runners
- **ih-aws** — AWS credential helpers and ECS utilities
```bash
pip install infrahouse-toolkit
```

📚 [Documentation](https://infrahouse-toolkit.readthedocs.io)

## 💼 Professional Services

Need help with your AWS infrastructure? InfraHouse offers:

- **🏗️ Secure Cloud Blueprint** — Production-ready AWS infrastructure setup
- **🔧 Managed Infrastructure** — 24/7 monitoring and support for $10K/month flat rate
- **🆘 Data Recovery** — MySQL/InnoDB data recovery services

[![Contact Us](https://img.shields.io/badge/Get%20a%20Quote-Contact%20Us-0066CC?style=for-the-badge)](https://infrahouse.com/contact)

## 📖 Documentation Standards

All our Terraform modules follow consistent standards:

- ✅ Published to [Terraform Registry](https://registry.terraform.io/namespaces/infrahouse)
- ✅ Comprehensive README with terraform-docs integration
- ✅ GitHub Pages documentation with MkDocs
- ✅ Working examples in `examples/` directory
- ✅ Integration tests with pytest-infrahouse
- ✅ Security scanning (OSV, tflint)
- ✅ Apache 2.0 license

## 🤝 Contributing

We welcome contributions! Each module repository has:

- Issue templates for bugs and feature requests
- Pull request templates
- CONTRIBUTING.md guidelines
- SECURITY.md for vulnerability reporting

## 📬 Contact

- 🌐 Website: [infrahouse.com](https://infrahouse.com)
- 📧 Email: [github@infrahouse.com](mailto:github@infrahouse.com)
- 💼 LinkedIn: [infrahouse-inc](https://www.linkedin.com/company/infrahouse-inc/)
- 📅 Schedule a call: [Book a meeting](https://meetings.hubspot.com/oleksandr-kuzminskyi)

---

<p align="center">
  <em>Empowering startups with scalable, cost-effective AWS infrastructure</em>
</p>
