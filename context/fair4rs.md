Impact: Adoption and implementation of the FAIR for Research Software principles will create
significant benefits for many stakeholders, including increased research reproducibility for research
organizations, better practices and more software usage for its developers, clarity for funders around
their own policies and requirements for software investments, and guidelines for publishers on
sharing requirements.
This work will be of value to software project owners, researchers, users of research data and
software, the scientific community, research software engineers, software developers who publish
their software, software catalog maintainers, repository managers, software preservation and
archival experts, policymakers who are responsible for defining digital policies, and organizations
that create, modify, manage, share, protect, and preserve research software, funders of research, and
others with an interest in the FAIR principles for research software.

abstract
To improve the sharing and reuse of research software, the FAIR for Research Software
(FAIR4RS) Working Group has applied the FAIR Guiding Principles for scientific data
management and stewardship to research software, bringing together existing and new
community efforts. Many of the FAIR Guiding Principles can be directly applied to research
software by treating software and data as similar digital research objects. However, specific
characteristics of software — such as its executability, composite nature, and continuous
evolution and versioning — make it necessary to revise and extend the principles.
This document presents the first version of the FAIR Principles for Research Software
(FAIR4RS Principles), and includes explanatory text to aid adoption. It is an outcome of the
FAIR for Research Software Working Group (FAIR4RS WG) based on community consultations
that started in 2019.
The FAIR for Research Software Working Group was jointly convened as a Research Data
Alliance (RDA) Working Group, FORCE11 Working Group, and Research Software Alliance
(ReSA) Task Force.
The RDA Software Source Code Interest Group is the maintenance home for the principles.
Concerns or queries about the principles can be raised at RDA plenary events organized by the
SSC IG, where there may be opportunities for adopters to report back on progress. The full
maintenance and retirement plan for the principles can be found on the RDA website.

Introduction
The concept of FAIR originated in the Netherlands during the 2014 Lorentz Workshop "Jointly
Designing a Data FAIRport"
, where participants formulated the FAIR data vision to optimize data
sharing and reuse by humans and machines. This vision supports existing communities that try
to realize and enable a situation where valuable scientific data is ‘FAIR’ in the sense of four
foundational principles: being Findable, Accessible, Interoperable and Reusable. These four
foundational principles, and 15 guiding principles that provide further detail, were published in
“The FAIR Guiding Principles for scientific data management and stewardship” (Wilkinson et al.,
2016, shortened to the FAIR Guiding Principles in the remainder of this document).
This document presents the first release of the FAIR Principles for Research Software
(shortened to the FAIR4RS Principles in the remainder of this document). This work is an
outcome of the FAIR4RS for Research Software Working Group (FAIR4RS WG) that was
established in 2020 with the aim of developing community-endorsed FAIR principles for
research software. The FAIR4RS Principles represent the consensus view of the research
software community after extensive consultation (Katz et al., 2021, Chue Hong et al., 2021a).
From the outset, the FAIR Guiding Principles were intended to be applicable to many kinds of
digital assets, not just datasets. A number of research communities and groups have been
considering how to apply aspects of FAIR to research software since 2017 (EC, 2018, EC &
EOSC EB, 2020, EC, 2020, Gruenpeter et al., 2020). Community-produced outcomes on
applying FAIR to research software produced before February 2020 can be found in the
Software Source Code identification Interest Group’s Wiki FAIR4Software reading resources1
.
Newer resources can be found in the FAIR4RS collection on Zenodo2 and the literature review
completed by the FAIR4RS Working Group (Chue Hong et al., 2021b, FAIR4RS WG, 2021).
The ultimate goal of FAIR is to increase the transparency, reproducibility, and reusability of
research. For this to happen, software needs to be well-described (by metadata), inspectable,
documented and appropriately structured so that it can be executed, replicated, built-upon,
combined, reinterpreted, reimplemented, and/or used in different settings. The FAIR4RS
Principles aim to guide software creators and owners on how to make their software FAIR. The
FAIR4RS Principles are also relevant to the larger ecosystem and various stakeholders that
support research software (e.g., repositories and registries).
The FAIR4RS WG is jointly led by members of the Research Software Alliance (ReSA), Future
Of Research Communications and E-Scholarship (FORCE11), and the Research Data Alliance
(RDA) communities. The FAIR4RS WG is a global and interdisciplinary community composed of
~250 members3 who have an interest in the application of FAIR principles to research software
and other research outputs. The members have diverse roles such as software users, software
developers and maintainers, academics, policy makers, infrastructure support staff, and funders.
1 https://www.rd-alliance.org/group/software-source-code-ig/wiki/fair4software-reading-materials
2 https://zenodo.org/communities/fair4rs
3 https://www.rd-alliance.org/node/69317/members
FAIR Principles for Research Software version 1.0 4
FAIR Principles for Research Software
The FAIR4RS WG define research software (Gruenpeter et al., 2021) as:
Research Software includes source code files, algorithms, scripts, computational workflows
and executables that were created during the research process or for a research purpose.
Software components (e.g., operating systems, libraries, dependencies, packages, scripts,
etc.) that are used for research but were not created during or with a clear research intent
should be considered software in research and not Research Software. This differentiation
may vary between disciplines.
The FAIR4RS Principles are:
F: Software, and its associated metadata, is easy for both humans and machines to find.
F1. Software is assigned a globally unique and persistent identifier.
● F1.1. Components of the software representing levels of granularity are assigned distinct identifiers.
● F1.2. Different versions of the software are assigned distinct identifiers.
F2. Software is described with rich metadata.
F3. Metadata clearly and explicitly include the identifier of the software they describe.
F4. Metadata are FAIR, searchable and indexable.
A: Software, and its metadata, is retrievable via standardized protocols.
A1. Software is retrievable by its identifier using a standardized communications protocol.
● A1.1. The protocol is open, free, and universally implementable.
● A1.2. The protocol allows for an authentication and authorization procedure, where necessary.
A2. Metadata are accessible, even when the software is no longer available.
I: Software interoperates with other software by exchanging data and/or metadata, and/or
through interaction via application programming interfaces (APIs), described through
standards.
I1. Software reads, writes and exchanges data in a way that meets domain-relevant community standards.
I2. Software includes qualified references to other objects.
R: Software is both usable (can be executed) and reusable (can be understood, modified, built
upon, or incorporated into other software).
R1. Software is described with a plurality of accurate and relevant attributes.
● R1.1. Software is given a clear and accessible license.
● R1.2. Software is associated with detailed provenance.
R2. Software includes qualified references to other software.
R3. Software meets domain-relevant community standards.
Table 1: The FAIR Principles for Research Software
FAIR Principles for Research Software version 1.0 5
Software as source code is the preferred form for applying the FAIR4RS Principles. But software
can occur in other forms which may be more useful for some communities or may simply be the
only way in which the owner is willing to deliver them. These other forms include binaries,
containers or software as a service, amongst others. Many of these alternate forms make sense
for applying many but not all of the FAIR4RS Principles. For instance the internal workings of
compiled binaries cannot be inspected or verified, but access to them may improve reuse by
end-user researchers. The FAIR4RS Principles can be applied to any research software,
regardless of the license.
In the remainder of this document, each of the FAIR4RS Principles is described in more detail.
First, each foundational principle (F, A, I and R) is described, followed by the numbered guiding
principles used to interpret the foundational principle.
● Text in bold is the text for the principles.
● Text in italics elaborates on the principle, explains the meaning of specific keywords,
discusses the ramifications of adopting the principle and cross-references interrelated
principles.
A comparison of the evolution of these principles from the original FAIR Guiding Principles for
scientific data management and stewardship (Wilkinson et al., 2016, with foundational principle
text taken from GO FAIR, 2018) through the Towards FAIR Principles for research software
(Lamprecht et al., 2020) and Taking a fresh look at FAIR for research software report (Katz,
Gruenpeter & Honeyman, 2021) and the drafts developed by the FAIR4RS WG (Chue Hong et
al., 2021a) to these published FAIR4RS Principles is provided in Appendix B.
As with the FAIR Guiding Principles, the FAIR4RS Principles are intended to be aspirational.
The application of the FAIR4RS Principles is the responsibility of the owners (who are often the
creators) of the software, not the users. Responsibility can be shared in the long-term with other
stewards and the applicability of the principles is the responsibility of the providers of the
infrastructure they use to fulfill them, e.g., appropriate repositories and registries. This must be
emphasized, as those producing the software are best placed to ensure they provide the
necessary information to make their work as FAIR as possible, and get credit for doing so in
return.
FAIR Principles for Research Software version 1.0 6
Findable
F: Software, and its associated metadata, is easy for both humans and machines to find.
For software to be findable, its associated metadata are readable by both humans and machines.
Metadata should follow domain-relevant community standards.
F1. Software is assigned a globally unique and persistent identifier.
A piece of software is given an identifier which is both globally unique (not used to identify any
other object, even on a different system) and persistent (long-lasting, including its resolution -
the ability to use it to get to the identified source). The use of globally unique and persistent
identifiers enables adherence to many of the other FAIR4RS Principles by removing ambiguity
(for humans and machines) around what software (or part of it) is being referenced.
Complexities around software granularity (the “level of detail being implemented”) and software
versions (the “changes between implementations”) are addressed by F1.1 and F1.2. This
principle also relates to enabling accessibility to software, specifically A1.
F1.1. Components of the software representing levels of granularity are assigned distinct
identifiers.
The use of identifiers for more than the software project (often synonymous with “software
concept” or “software product”) improves findability by enabling components to be assigned
distinct identifiers e.g, a software library, and a function in that library. The relationship between
these components is embodied in the associated metadata. Granularity levels for software are
shown in Figure 1 in Appendix A. These principles do not prescribe which granularity levels
should be assigned identifiers, as this is likely to be implementation-specific.
F1.2. Different versions of the software are assigned distinct identifiers.
To make different versions of the same software (or component) findable, each version needs to
be assigned a different identifier. The relationship between versions is embodied in the
associated metadata. What is considered a “version” is defined by the owner of the software: in
many cases this will be something that the owner wants to specifically identify and use and/or
“release” or “publish” so that others can use and reference/cite.
There are existing software engineering practices (e.g., version control, semantic versioning)
around the management and versioning of software that may form part of the implementation of
these relationships.
FAIR Principles for Research Software version 1.0 7
Capturing the relationships between different versions of software will lead to greater
understanding of the evolution of code, its authorship, ownership, description and purpose,
amongst other things.
F2. Software is described with rich metadata.
Software requires descriptive metadata to support indexing, search and discoverability. This
metadata must itself be FAIR (F4), should follow community standards, and use controlled
vocabularies. The FAIR4RS principles do not define which standards should be used, as this is
better captured in guidance for implementing the principles coming out of each community. R1,
R1.1, and R1.2 describe categories of metadata that enable reuse.
F3. Metadata clearly and explicitly include the identifier of the software they describe.
The association between the metadata (wherever it is stored; see F4) and the software should
be made explicit by mentioning the software’s globally unique and persistent identifier in its
associated metadata. In conjunction with A1, this means the metadata describes how the
software can be obtained. Metadata are not required to include references for all of the
softwares dependencies in order for software to be findable. I2 and R2 describe how references
to dependencies increase the likelihood that software is interoperable and reusable.
F4. Metadata are FAIR, searchable and indexable.
Making the metadata about the software FAIR, including making it readable and discoverable by
both humans and machines, improves the findability of software by supporting searching and
indexing by others. It allows the metadata to be published in or harvested by a registry or
catalog or repository, or by a search engine. FAIR metadata also enables and encourages
citation of research software.
Accessible
A: Software, and its metadata, is retrievable via standardized protocols.
In the FAIR Guiding Principles, accessibility translates into retrievability. In these FAIR4RS
Principles, accessibility is also narrowly scoped to the ability to “retrieve” the software. Because
software by necessity requires the use of standardized communications protocols to operate,
some of the FAIR Guiding Principles may be considered commonly understood and
implemented for software.
For software to be accessible, it may be made available in any form (including, but not limited to
source code, executable, library, or service) as long as the conditions for access are clearly
FAIR Principles for Research Software version 1.0 8
stated and transparent. The software should be retrievable by both humans and machines or, in
the case of software as a service, the software functionality is accessible via standardized
protocols.
In software engineering,
“accessibility” can also be used to refer to the ability to access or use
the software regardless of impairment, e.g. a disability. While this is important for research
software, this is not how the original FAIR Guiding Principles define accessibility. It is
recommended that the practice of making software usable by as many people as possible is
best addressed in R3, and as separate guidance complementing the FAIR4RS Principles.
A1. Software is retrievable by its identifier using a standardized communications
protocol.
Different types of software have different methods for access. For instance, software that is only
available in source code form may be downloaded from a repository before being compiled
locally, whereas software hosted as a service on a remote server may be accessed without
retrieving it. This principle states that obtaining the software should not require specialized or
proprietary tools or communication methods. For much software, there are commonly used
technical communications protocols used to access the software, such as HTTPS.
A1.1. The protocol is open, free, and universally implementable.
It is the openness of the communications protocol (including the resolver for the identifier) that is
important, not the implementation of the infrastructure that supports it. Here “open” means that
there are no restrictions to implementing it and “free” means that there are no fees or licensing
costs to implement it.
A1.2. The protocol allows for an authentication and authorization procedure, where
necessary.
The FAIR Guiding Principles put specific emphasis on enhancing the ability of machines to use
digital objects. In the context of software, there are often conditions of access, for instance,
requiring a license server to be contacted, requirement for payment before use, or restrictions
based on the privilege level of the user.
A2. Metadata are accessible, even when the software is no longer available.
Availability of software may change over time, because there is a cost to maintaining access or
because the software has degraded and is no longer safely usable, or because dependencies
are no longer available. The metadata describing the software is generally easier and cheaper
FAIR Principles for Research Software version 1.0 9
to store and maintain than the software itself (e.g., in the software repository, or in a software
registry or catalog) and there is value in understanding the details of the software even if it is no
longer accessible.
Interoperable
I: Software interoperates with other software by exchanging data and/or metadata, and/or
through interaction via application programming interfaces (APIs), described through
standards.
The definitions of interoperability and reusability as defined by the FAIR Guiding Principles
overlap when applied to software. To differentiate between the two, interoperability here is
limited to being concerned with the capacity to exchange data between independent software
(i.e., software that can be executed separately). As an example, the sense of “integrated” that
applies to data (where two pieces of data combine to form new data) does not apply in the same
way to software where, in a sense, all software is “integrated” with, or depends on, other
software (and this concept is placed under reusability, in R2). Software also has “agency”:
software calls on other software. Two independent pieces of software can be said to
interoperate when the functionality exists in both to read and write or otherwise exchange data.
I1. Software reads, writes and exchanges data in a way that meets domain-relevant
community standards.
Software interoperates through the exchange of data. This includes the use of data and
metadata types, controlled vocabularies, and formats that are formally defined through
standards to facilitate the exchange. Whereas F4 requires that metadata describing the
software are FAIR, this principle ensures that the way that software interacts with other software
is clearly described. A domain-relevant standard is an agreed standard that addresses the
needs of a given community (or communities). Examples of community standards for data are
curated by the FAIRSharing Registry at https://fairsharing.org/standards/.
Where software interacts via APIs, these should be documented so that their capabilities can be
inspected and understood by humans and machines, and they should be open APIs where
possible.
I2. Software includes qualified references to other objects.
Some software includes references to external data objects required to execute the software
(e.g., parameter files for certain applications). Ideally, the data would be FAIR as well, and
references to external data would be fully qualified. Qualified references should be to digital
objects (e.g., metadata, other software, data), as well as to non-digital objects that have a virtual
FAIR Principles for Research Software version 1.0 10
presence in digital systems (e.g., samples, reagents, instruments, etc.) with which the software
interacts. These qualified references should be described using identifiers and/or controlled
vocabularies.
“Qualified” means specifying the authoritative source for an identifier or
vocabulary item, possibly including a resolvable reference to further information about the
source. Ideally this is in a form that includes a resolver within the reference (e.g., in the form of a
persistent identifier, or URL). This information can also improve the reusability of software by
explicitly including references to articles and data sets that document its use. Examples of
qualified references might include: software X is implemented using software A (a programming
language); software X uses software B (a library/dependency); software X is tested within
software C (a platform); software X extends software D.
Reusable
R: Software is both usable (can be executed) and reusable (can be understood, modified,
built upon, or incorporated into other software).
The definitions of interoperability and reusability as defined by the FAIR Guiding Principles
overlap when applied to software. To differentiate between the two, reusability (implicitly
including usability) here focuses on the ability of humans and machines to execute, inspect, and
understand the software, so it can be modified, built upon, or incorporated into other software.
Note that the general intent of these principles is that software is “executable in principle”
- not
“guaranteed to execute”
. Also, different aspects of reusability may best apply to different forms
of software. The form in which it is made available changes the way it can be used. For
instance, source code might be modifiable but not executable without specialist infrastructure;
libraries available as binaries can be built on and incorporated into other software but not easily
modified. In general, source code is the most reusable form of software.
The concept of software quality overlaps with the FAIR4RS Principles, particularly reusability,
but is not directly addressed by them. Similar to openness, software quality is beneficial to
making software FAIR but not required.
R1. Software is described with a plurality of accurate and relevant attributes.
It is easier to reuse (and find) software if there are many descriptive labels attached to it. F2
requires software to be described by rich metadata. References provided by applying I2 can
help document the use and purpose of the software. Software should be described for the
categories of R1.1 (license), R1.2 (provenance), and additionally address the categories of
metadata that facilitate reuse. Relevant attributes can be determined by repositories, and by
communities who create and reuse software. Plurality means that, where possible, multiple
terms for the same, similar, or overlapping concepts should be provided to enable the broadest
possible reuse.
FAIR Principles for Research Software version 1.0 11
Metadata and documentation are distinct, potentially complementary, concepts. Metadata about
software can be included in documentation, or in the code itself, or in a separate location.
Metadata included in the documentation are generally not machine readable, or indexable. This
does, however, support the reusability of software particularly from a human perspective.
R1.1. Software is given a clear and accessible license.
To enable reuse, software must have a license that clearly describes how it can be used and
reused, ideally with conditions that are readable by humans and machines. Licenses are often
referred to by name, but machine readable licenses can be specified by reference to a standard
vocabulary such as the SPDX License List4 (SPDX Consortium, 2020). To support a wide range
of reuse scenarios, the license should be as unrestrictive as possible and, to avoid license
proliferation, choosing a widely used and recognized license is strongly recommended. This
license must also be compatible with the requirements of the licenses of the software’s
dependencies so that the software can be legally combined.
R1.2. Software is associated with detailed provenance.
Software provenance is a type of metadata that describes why and how the software came to
be, as well as who contributed what, when and where. Provenance is sometimes referred to as
lineage or pedigree. This extends beyond capturing a log of changes to source code as it is
developed. Good provenance metadata clarifies the origins and intent behind the development
of the software, and establishes authenticity and trust. As a type of metadata this overlaps with
the metadata called for in guiding principles F2 and F4.
R2. Software includes qualified references to other software.
Software is rarely standalone and in most cases is built upon other software (e.g.,
dependencies), it should include appropriate references to other software (e.g., requirements,
imports, libraries) which are necessary to compile and run the software.
“Qualified” here means
specifying the authoritative source for an identifier, possibly including a resolvable reference to
further information about the source. To follow this principle, it is desirable but not required that
the other software referenced implements the FAIR4RS Principles. In many programming
languages, base methods or functions take a reference to a named entity, possibly in
combination with a version number or qualifying domain and resolves this to a source. This
principle goes beyond this in calling for qualified references to external dependencies, meaning
that the reference itself resolves to the source via the qualifying authority.
4 https://spdx.org/licenses/
FAIR Principles for Research Software version 1.0 12
This guiding principle calls for qualified references in software to other software (in aid of reuse).
Principle I2 calls for qualified references to anything other than software (in aid of
interoperability).
R3. Software meets domain-relevant community standards.
Software, including its documentation and license, should meet domain-relevant community
standards and coding practices (e.g., choice of programming language, standards for testing,
usage of file formats, accessibility [in the sense of usable by as many people as possible]) that
enable reuse. While the FAIR4RS Principles do not specify particular community standards, the
intent is to ensure that practitioners are aware of what others are doing and using in the
community, e.g., through initiatives like FAIRsharing (Sansone et al., 2019), whilst
acknowledging that community standards are (and should be) under constant development.
Communities can encompass research domains, programming languages, and technical
approaches. Examples of community standards might include: BioSchemas from ELIXIR for
describing resources in the life sciences and schema.org for general description of resources;
Common Workflow Language; and the package managers commonly used by a programming
language such as Maven (Java), npm (Javascript), PyPI (Python) and CRAN (R). It is important
to note that the FAIR Guiding Principles address research outputs, not research processes, so
standards should also be limited to best practice about the software itself, not the process of
designing, developing, or maintaining it, such as the R community standards for creating
packages5 or the PEP 8 Style Guide for Python Code
.