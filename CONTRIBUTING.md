# Contributing to Digital Product Passport on Cardano

This repository is maintained by a working group of companies implementing DPP solutions on Cardano. We welcome community contributions.

Please review our [Code of Conduct](CODE-OF-CONDUCT.md) before contributing.

## Table of Contents

- [Contribution Types](#contribution-types)
- [Submission Process](#submission-process)
- [Style Guidelines](#style-guidelines)
- [Working Group](#working-group)

## Contribution Types

### 1. User Personas
Add new industry-specific personas or enhance existing ones with implementation feedback.

**Location**: `personas.md`

**Format**: Add to existing document following the established structure

**Required sections**:
- Name, Age, Job Title, Company Type, Example Companies
- Description
- Primary Need
- Profile and Goals
- Key Requirements (bulleted list)
- Pain Points

### 2. Solution Patterns
Propose new architectural patterns or optimize existing ones.

**Location**: `DPP-Blueprint-Cardano-v0.1.md`

**Format**: Add to appropriate section in blueprint document

**Required sections**: Overview, When to Use, Architecture, Implementation Steps, Code Examples, Cost Analysis, Security, Scalability, Compliance Mapping

### 3. Code Examples
Provide working implementation samples.

**Format**: Add inline to blueprint document or create separate files if substantial

**Requirements**:
- Commented code explaining DPP-specific logic
- Sample input/output
- Error handling
- Setup/usage instructions

### 4. Standards & Compliance
Update documentation when regulations or standards change.

**Location**: `DPP-Blueprint-Cardano-v0.1.md` or `README.md`

**Include**: What changed, effective date, impact analysis, migration path

### 5. Case Studies
Share real-world implementation experiences.

**Format**: Add to blueprint document or create separate markdown file

**Required sections**: Executive Summary, Company Profile, Challenge, Solution, Results, Lessons Learned, Recommendations

## Submission Process

### Setup
```bash
git clone https://github.com/[your-username]/dpp-cardano.git
cd dpp-cardano
git checkout -b feature/your-contribution
# Make changes
git commit -m "feat: description"
git push origin feature/your-contribution
```

### Pull Request

**Title format**:
```
feat: Add textile recycling persona
docs: Update cost analysis
fix: Correct Merkle proof example
example: Add SAP integration
```

**PR template**:
```markdown
## Description
[What does this PR do?]

## Type
- [ ] Persona
- [ ] Pattern
- [ ] Code example
- [ ] Documentation
- [ ] Standards update
- [ ] Case study

## Testing
[Testnet transaction IDs if applicable]

## Checklist
- [ ] Follows style guidelines
- [ ] Documentation included
- [ ] Code tested
- [ ] No sensitive information
- [ ] ESPR aligned
```

### Commit Messages
Use conventional commits:
- `feat`: New feature/persona
- `fix`: Bug fix
- `docs`: Documentation
- `example`: Code example
- `chore`: Maintenance

## Style Guidelines

### Documentation
- Use clear heading hierarchy (##, ###)
- Include code blocks with language specification
- Add diagrams where helpful (Mermaid preferred)
- Use tables for comparisons
- Professional but accessible tone

### Code
- Prioritize readability
- Include comments explaining DPP-specific logic
- Handle errors gracefully
- Follow language-specific conventions

## Working Group
The working group consists of **companies actively implementing DPP solutions on Cardano** in production or advanced pilot stages.

#### What Working Group Members Do:

- Share implementation experiences and challenges
- Influence architectural direction
- Provide feedback on community contributions
- Participate in monthly technical Q&A sessions (optional but encouraged)
- Collaborate on standards alignment

**Meetings**: 60 minutes, once per month

**To Join**: Open an issue titled "Working Group Participation Request" with your organization, role, industry focus, and implementation status.

## Review Process

- **Initial review**: 5 business days
- **Technical review**: 7-10 business days
- **Working group review**: Next monthly meeting for major changes

**Criteria**: ESPR alignment, practical value, code quality, documentation standards

## Recognition

Contributors are acknowledged in README, specific pages, and working group notes. 

By contributing, you agree that your contributions will be licensed under the same terms as described in [LICENSE.md](LICENSE.md).

## Support

- **Questions**: Open GitHub issue with `question` label
- **Compliance**: Use `compliance` label
- **Discussion**: GitHub Discussions

---

**Ready to contribute?** Fork the repository and submit your PR.

For questions, open an issue or join our next working group meeting.
