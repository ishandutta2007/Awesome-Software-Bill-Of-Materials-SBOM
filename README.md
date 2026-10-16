# Awesome-Software-Bill-Of-Materials-SBOM

## Top Software-Defined Storage Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Distributed File Systems, Unified Storage & Cloud-Native Block Storage*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Software-Defined Storage**. These tools decouple storage software from physical hardware, enabling organizations to build scalable, resilient storage clusters from commodity servers — spanning file, block, and object storage interfaces.

**Examples** include AWS EFS, Azure Files, Google Cloud Filestore, NetApp Cloud Volumes ONTAP, Pure Storage FlashBlade, Qumulo Cloud, Dell PowerScale, GlusterFS, CephFS, and IBM Spectrum Scale (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, distributed metadata management, and transparent storage architecture — ideal for infrastructure teams prioritizing hardware independence, avoiding proprietary lock-in, and building storage that scales with commodity hardware.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[AWS EFS](https://aws.amazon.com/efs/)**  
  Fully managed, elastic NFS file system for AWS. Scales automatically as files are added and removed, with no capacity planning required. **Regional and One Zone** storage classes; supports POSIX permissions and NFSv4.1. Integrated with AWS IAM and VPC security groups.

- **[Azure Files](https://azure.microsoft.com/en-us/products/storage/files/)**  
  Fully managed file shares in the cloud using SMB and NFS protocols. Supports Windows, Linux, and macOS clients with AD integration for identity-based access. **Premium tier** uses SSD-backed storage for high-throughput workloads.

- **[Google Cloud Filestore](https://cloud.google.com/filestore)**  
  Fully managed NFS file storage for GCP. **Basic, High Scale, and Enterprise tiers** — Enterprise supports multi-share and larger capacity for demanding workloads. Integrated with GKE via CSI driver for persistent volume provisioning [citation:11].

- **[NetApp Cloud Volumes ONTAP](https://www.netapp.com/cloud/)**  
  Managed ONTAP file service available on AWS, Azure, and Google Cloud. **Lift-and-shift** Linux and Windows applications to cloud, consolidate file servers, and extend on-premises ONTAP to cloud. Controlled via **NetApp BlueXP** [citation:6].

- **[Dell PowerScale for Multi-Cloud](https://www.dell.com/)**  
  OneFS-based scale-out NAS available on AWS, Azure, and Google Cloud (via Faction and Sycomp). Provides multi-cloud data services with shared namespace and high-performance file access [citation:6].

- **[IBM Spectrum Scale](https://www.ibm.com/products/storage-scale)**  
  High-performance, high-availability clustered file system available on AWS, Azure, and GCP. Provides shared namespace across multiple instances without requiring deep Spectrum Scale expertise. Cloud-kit preview enables CLI-driven cluster deployment on Azure [citation:6].

- **[Pure Storage FlashBlade](https://www.purestorage.com/)**  
  Unified fast file and object storage platform. **Cloud Block Store** available on AWS and Azure for workload portability [citation:6].

- **[Qumulo Cloud](https://qumulo.com/)**  
  Cloud-native file data platform with real-time analytics and multi-protocol support.

## Open-Source GitHub Projects

- **[Ceph](https://github.com/ceph/ceph)**  
  **The unified distributed storage platform** — 14,000+ GitHub stars, LGPL-2.1 licensed. Provides **three storage interfaces in one system**: **CephFS** (POSIX file system), **RBD** (block devices), and **RGW** (object storage gateway) [citation:1][citation:5]. **CephFS** stores file metadata in a separate RADOS pool served by a resizable cluster of **Metadata Servers (MDS)** — clients have direct access to RADOS for data I/O with no gateway or broker [citation:5]. **Rook** deploys Ceph on Kubernetes with CSI drivers for dynamic volume provisioning and ReadWriteMany access [citation:7]. **The most widely deployed open-source SDS platform** for cloud infrastructure and Kubernetes storage.

- **[MooseFS](https://github.com/moosefs/moosefs)**  
  **Petabyte-scale distributed file system** — 1,700+ GitHub stars, GPL licensed. **Pure C implementation** with **no single point of failure** — all components can be redundant [citation:2]. **Configurable replication per file**, dynamic capacity expansion by adding servers/disks on the fly, **file system-level trash bin** with configurable retention, **atomic snapshots** even during writes, **IP/password access control** (like NFS), **data tiering** via Storage Classes, and **per-directory project quotas** [citation:2]. Supports block storage via `mfsbdev`. Available on Debian, Ubuntu, RHEL, Rocky Linux, AlmaLinux, Fedora, OpenSUSE, Arch, Alpine, FreeBSD, and macOS [citation:2][citation:13]. **The most feature-complete alternative to GlusterFS** for scalable NAS workloads.

- **[GlusterFS](https://github.com/gluster/glusterfs)**  
  **Scalable, highly available network filesystem** — designed to scale out and handle large amounts of data across compute instances [citation:4]. Replicates data across multiple GlusterFS servers into a **single application mount point**, providing high availability and fault tolerance [citation:4]. **Flexible architecture** supports cloud storage and HA architectures. **Note**: GlusterFS development has slowed significantly — evaluate MooseFS or CephFS for new deployments.

- **[LizardFS](https://github.com/lizardfs/lizardfs)**  
  **Highly reliable, scalable, and efficient distributed file system** — GPLv3 licensed [citation:9]. Spreads data over physical servers as a single file system. **Successor to MooseFS** with additional features. Available in FreeBSD ports [citation:9]. **Note**: Development has slowed — MooseFS remains more actively maintained.

- **[LINSTOR](https://github.com/LINBIT/linstor-server)**  
  **High-performance software-defined block storage** for containers, cloud, and virtualization — Java-based, fully integrated with Docker, Kubernetes, OpenStack, and Proxmox [citation:1][citation:12]. **The block storage layer for Kubernetes** when you need replicated persistent volumes without a full Ceph deployment.

- **[OpenEBS](https://github.com/openebs/openebs)**  
  **Most popular container-native storage platform for Kubernetes** — 8,900+ GitHub stars [citation:12]. Provides replicated, highly available persistent volumes for stateful applications with CSI driver integration. **Alternative to Ceph for Kubernetes-only deployments** where full unified storage is overkill.

- **[DAOS](https://github.com/daos-stack/daos)**  
  **Distributed Asynchronous Object Storage** from Intel — 763+ GitHub stars [citation:1]. **High-performance storage stack** for HPC and AI workloads with client libraries, storage engine, and control plane. **Optimized for NVMe and persistent memory**.

- **[Sheepdog](https://github.com/sheepdog/sheepdog)**  
  **Distributed storage system for QEMU** — 988+ GitHub stars [citation:1]. Provides replicated block storage for virtual machines. **Note**: Development has been inactive for several years.

- **[Curve](https://github.com/opencurve/curve)**  
  **Cloud-native distributed storage system** hosted by CNCF — 2,300+ GitHub stars [citation:12]. Supports block and shared file storage with high performance and easy operation.

- **[OpenIO SDS](https://github.com/open-io/oio-sds)**  
  **High-performance software-defined object storage** for Big Data and AI — supports Amazon S3 and OpenStack Swift APIs [citation:1].

- **[ZapFS](https://github.com/LeeDigitalWorks/zapfs)**  
  **Open-core distributed object storage system** — Apache 2.0 core with commercial enterprise features [citation:14]. Supports S3-compatible API with bucket/object CRUD, multipart upload, versioning, ACLs, and policies. **Distributed architecture** with manager (Raft consensus), metadata (Vitess/MySQL/PostgreSQL), and file services. **Dual licensing model** — community edition for free use, enterprise for advanced features [citation:14].

### Additional Strong Open-Source Options

- **BeeGFS** — High-performance parallel file system for HPC with metadata server separation, RDMA support, and BeeOND on-demand clustering [citation:16].
- **SeaweedFS** — Fast distributed object storage optimized for small files. S3-compatible with erasure coding.
- **MinIO** — High-performance S3-compatible object storage. AGPL licensed with commercial licensing available.
- **CubeFS** — CNCF distributed file and object storage system.
- **FoundationDB Block Device** — Replicated block device backed by FoundationDB.

**Frameworks for building custom systems**: Combine **CephFS** for unified file, block, and object storage with direct RADOS client access, **MooseFS** for petabyte-scale POSIX file system with per-file replication and snapshots, **LINSTOR** or **OpenEBS** for Kubernetes-native block storage, and **BeeGFS** for HPC parallel workloads — to build a complete software-defined storage stack spanning NAS, SAN, and object use cases from commodity hardware.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Software-defined storage tools differ significantly in architecture, protocol support, and operational complexity. **Ceph is the most widely deployed** but has the steepest learning curve — a full unified storage platform with MDS, OSD, MON, and MGR daemons to manage [citation:5]. **MooseFS offers the richest feature set for NAS use cases** including file-level trash, atomic snapshots, and per-directory quotas [citation:2]. **GlusterFS and LizardFS have slowed development** — evaluate MooseFS or CephFS for new projects. **Cloud-managed services (EFS, Azure Files, Filestore) eliminate operational burden** at the cost of vendor lock-in and per-GB pricing. **Managed NetApp, Dell, and IBM offerings provide enterprise features with cloud elasticity** but are proprietary [citation:6].
- Self-hosted open-source solutions require proper cluster planning, redundancy configuration, monitoring, and backup strategies. Distributed storage is not a substitute for backups — replication protects against hardware failure, not accidental deletion or corruption.

---

**Made for infrastructure engineers, storage architects, DevOps teams, and developers building scalable storage platforms.**  
Let's make software-defined storage more open, resilient, and hardware-independent.
