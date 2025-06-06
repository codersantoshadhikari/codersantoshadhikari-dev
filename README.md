<div align="center">

[crates-shield]: https://img.shields.io/crates/v/soar-cli
[crates-url]: https://crates.io/crates/soar-cli
[discord-shield]: https://img.shields.io/discord/1313385177703256064?logo=%235865F2&label=discord
[discord-url]: https://discord.gg/djJUs48Zbu
[doc-shield]: https://img.shields.io/badge/docs-soar.qaidvoid.dev-blue
[doc-url]: https://soar.qaidvoid.dev
[issues-shield]: https://img.shields.io/github/issues/pkgforge/soar.svg
[issues-url]: https://github.com/pkgforge/soar/issues
[license-shield]: https://img.shields.io/github/license/pkgforge/soar.svg
[license-url]: https://github.com/pkgforge/soar/blob/main/LICENSE
[packages-shield]: https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/pkgforge/metadata/refs/heads/main/TOTAL_INSTALLABLE.json&query=$[6].total&label=packages&labelColor=grey&style=flat&link=https://pkgs.pkgforge.dev
[packages-url]: https://pkgs.pkgforge.dev
[stars-shield]: https://img.shields.io/github/stars/pkgforge/soar.svg
[stars-url]: https://github.com/pkgforge/soar/stargazers

[![Crates.io][crates-shield]][crates-url]
[![Discord][discord-shield]][discord-url]
[![Documentation][doc-shield]][doc-url]
[![Issues][issues-shield]][issues-url]
[![License: MIT][license-shield]][license-url]
[![Packages][packages-shield]][packages-url]
[![Stars][stars-shield]][stars-url]

</div>

<p align="center">
    <a href="https://soar.qaidvoid.dev/installation">
        <img src="https://soar.pkgforge.dev/gif?version=v0.5.15+1" alt="soar-list" width="750">
    </a><br>
</p>

<h4 align="center">
  <a href="https://soar.qaidvoid.dev">📘 Documentation</a> |
  <a href="https://docs.pkgforge.dev">🔮 PackageForge</a>
</h4>

<p align="center">
    Soar is a Fast, Modern, Bloat-Free Distro-Independent Package Manager that <a href="https://docs.pkgforge.dev/soar/comparisons"> <i>Just Works</i></a><br>
    Supports <a href="https://docs.pkgforge.dev/formats/binaries/static">Static Binaries</a>, <a href="https://docs.pkgforge.dev/formats/packages/appimage">AppImages</a>, and other <a href="https://docs.pkgforge.dev/formats/packages">Portable formats</a> on any <a href="https://docs.pkgforge.dev/repositories/soarpkgs/faq#portability"><i>*Unix-based</i> Distro</a>
</p>


## 🪄 Quickstart

> [!TIP]
> - Soar comes as a single-file, statically-linked executable with no dependencies that you can simply [download](https://github.com/pkgforge/soar/releases/latest) & run.
> - The [install script](https://github.com/pkgforge/soar/blob/main/install.sh) does this & more automatically for you.
 
```bash
❯ cURL
curl -fsSL "https://raw.githubusercontent.com/pkgforge/soar/main/install.sh" | sh

❯ wget
wget -qO- "https://raw.githubusercontent.com/pkgforge/soar/main/install.sh" | sh
```

> [!NOTE]
> - Please read & verify what's inside the script before running it
> - The script is also available through https://soar.qaidvoid.dev/install.sh & https://soar.pkgforge.dev/install.sh
> - Additionally, if you want to customize your installation, please read the docs @ https://soar.qaidvoid.dev/installation.html
> - For, extra Guide & Information on infra backends & adding more repos: https://docs.pkgforge.dev
> - Next, Check [Configuration](https://soar.qaidvoid.dev/configuration) & [Usage](https://soar.qaidvoid.dev/package-management)

## 🌟 Key Features

> [!TIP]
> - The comparison page @ https://docs.pkgforge.dev/soar/readme goes into more detail.

| Feature | Description |
|:--:|:--|
| **Universal Package Format Support** | Soar can install and manage portable package formats including [static binaries](https://docs.pkgforge.dev/formats/binaries/static), [self-extractable archives](https://docs.pkgforge.dev/formats/packages/archive), and [AppImages](https://docs.pkgforge.dev/formats/packages/appimage). |
| **System Integration** | Soar [automatically integrates](https://soar.qaidvoid.dev/#desktop-integration) installed packages with your system to provide a native-like experience. |
| **Flexible Repository System** | While Soar comes preconfigured with [official repositories](https://docs.pkgforge.dev/repositories), you can [configure custom repositories](https://soar.qaidvoid.dev/configuration#custom-repository-support) that use any build format as long as they provide compatible metadata. The `.SBUILD` format is only required for the official repositories, not for custom ones. |
| **Security First** | Soar enforces security through checksums and signing verification for package installations. |
| **Userspace** | Soar works completely in Userspace without Superuser (admin/sudo) Privileges. |
| **External Repository Support** | Soar can access packages from sources like [ivan-hc/AM](https://github.com/ivan-hc/AM) and [appimage.github.io](https://github.com/AppImage/appimage.github.io) through metadata provided by pkgforge. These external sources don't directly work with soar but are made compatible through pkgforge's metadata conversion. **Note:** Packages from external repositories are not verified. |
| **Fast Package Operations** | Soar provides efficient package searching, installation, and management with minimal overhead. |

## 📦 Packages

> [!TIP]
> Check out the detailed documentation @ https://docs.pkgforge.dev/repositories/soarpkgs

| Feature | Description |
|:--:|:--|
| **Portable Packages** | Packages are designed to be [portable](https://docs.pkgforge.dev/formats/) across distributions, either through [static linking](https://docs.pkgforge.dev/formats/binaries/static) or by bundling all dependencies. This makes them [distro-agnostic](https://docs.pkgforge.dev/soar/readme/packages#portability). |
| **Extensive Collection** | Official repositories host one of the [largest collections](https://docs.pkgforge.dev/soar/readme/packages#total) of portable packages. Browse them with `soar list` or at [pkgs.pkgforge.dev](https://pkgs.pkgforge.dev/). |
| **Prebuilt Binaries** | 100% of official packages are provided as [prebuilts](https://docs.pkgforge.dev/repositories/soarpkgs/faq#cache), making installation limited only by download speed. |
| **Quality Compilation** | Around 80% of packages are compiled from source with optimizations for performance (LTO), security (ASLR/PIE), and size (MUSL). |
| **High Security Standards** | Official packages are built with [SLSA Build L2 Security Guarantees](https://docs.pkgforge.dev/soar/readme/security). |
| **Community Contributions** | The [`.SBUILD`](https://docs.pkgforge.dev/sbuild/introduction) format in [pkgforge/soarpkgs](https://github.com/pkgforge/soarpkgs) allows community members to submit package definitions, similar to AUR. |
| **Cross-Distro Compatibility** | Some packages are repackaged from other distro repositories, allowing you to run applications from e.g., Arch repositories on Debian-based systems without containers. |
| **Decentralized** | The portable nature of packages means they can be downloaded and used independently of Soar if needed. |







## ``````````````````````````````````````````````````##
<div align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExcGJ1a2R2b2F5dG1xY3J4d3J2eGZ6Y2V6d2V6bGJ4aGx1ZzV1aGJ5ZyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/qgQUggAC3Pfv687qPC/giphy.gif" width="800" alt="Code Animation"/>
</div>

<h1 align="center">Santosh Adhikari</h1>
<h2 align="center">Senior Mobile App Developer & Technical Founder</h2>

<div align="center">
  <a href="https://santoshadhikari.info.np">
    <img src="https://img.shields.io/badge/🌐_Portfolio-00C4B4?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Portfolio"/>
  </a>
  <a href="https://play.google.com/store/apps/dev?id=8310692885659472367">
    <img src="https://img.shields.io/badge/📱_Play_Store-414141?style=for-the-badge&logo=google-play&logoColor=white" alt="Play Store"/>
  </a>
  <a href="https://www.smaittechnology.com.np">
    <img src="https://img.shields.io/badge/🚀_SMAIT_Technology-FF6F61?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Company"/>
  </a>
</div>

---

## 👨‍💻 Professional Profile

**Innovative Software Developer** with **6+ years** of specialized experience in mobile application development. As **Founder of SMAIT Technology**, I've led the creation of **60+ applications** with **15+ currently published** on app stores. My passion lies in building technical solutions that bridge digital innovation with real-world impact.

**Core Competencies:**
- Mobile App Development (Flutter, React Native, Kotlin)
- Full-Stack Development (Node.js, Firebase, MongoDB)
- Game Development (Unity, Ludo Game Specialist)
- Ethical Hacking & Security (MBA Certified)
- Startup Leadership & Technical Management

---

## 🏆 Key Achievements

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 30px 0;">

### 🚀 Published Applications
- **60+ applications** developed
- **15+ live apps** on Play Store/App Store
- Featured **Ludo gaming application** with 10K+ downloads

### 🎓 Education & Certification
- **MBA in Ethical Hacking** - Cybersecurity specialization
- **Mobile Development Certifications** - Flutter, React Native
- **Continuous learning** in emerging technologies

### 🏢 SMAIT Technology
- Founded and scaled tech startup
- Innovating games, apps, and software solutions
- Building a smarter digital world through technology

</div>

---

## 🎮 Featured Project: Ludo Game

[![Ludo Game](https://img.shields.io/badge/🎮_Ludo_Game-FF6F61?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=np.smaittechnology.ludo)

**Key Features:**
- Multiplayer online gameplay
- Smooth 60FPS performance
- Secure authentication system
- Real-time matchmaking

**Technologies Used:**
- Unity Game Engine
- Firebase Realtime Database
- Google Play Services
- In-app purchase integration

---

## 🛠️ Technical Stack

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin: 30px 0;">

### 📱 Mobile Development
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![Kotlin](https://img.shields.io/badge/Kotlin-0095D5?style=flat-square&logo=kotlin&logoColor=white)

### 🎮 Game Development
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white)

### ☁️ Backend & Database
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

### 🔒 Security
![Ethical Hacking](https://img.shields.io/badge/Ethical_Hacking-FF6F61?style=flat-square&logo=lock&logoColor=white)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-0078D7?style=flat-square&logo=shield-check&logoColor=white)

</div>

---

## 🌟 Why Work With Me?

- **Proven Track Record**: 60+ successful applications
- **Full-Cycle Development**: From concept to publication
- **Security-Focused**: MBA in Ethical Hacking ensures secure apps
- **User-Centric Design**: Apps with high retention rates
- **Technical Leadership**: Founder managing development teams

---

<div align="center">
  <h2>📬 Let's Connect</h2>
  <p>I'm always open to discussing new projects, creative ideas, or opportunities to collaborate</p>
  
  <div style="margin: 30px 0;">
    <a href="mailto:santosh.ad215@gmail.com">
      <img src="https://img.shields.io/badge/✉️_Email-FF6F61?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
    </a>
    <a href="https://linkedin.com/in/codersantoshadhikari">
      <img src="https://img.shields.io/badge/💼_LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
    </a>
    <a href="https://play.google.com/store/apps/dev?id=8310692885659472367">
      <img src="https://img.shields.io/badge/📱_Play_Store-414141?style=for-the-badge&logo=google-play&logoColor=white" alt="Play Store"/>
    </a>
  </div>
</div>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=00C4B4&height=120&section=footer&animation=fadeIn&fontSize=40" alt="Footer wave"/>
</div>

