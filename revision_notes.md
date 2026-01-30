# 📝 QUICK REVISION NOTES: Knowledge Representation & OWL
## Copy These for Your Exam!

---

## 🎯 THE BIG PICTURE (Memorize This!)

```
Human reads websites → Web of DOCUMENTS
Computer reads data  → Web of DATA (needs special format!)

RDF → RDFS → OWL (each one is more powerful!)
```

---

## 1️⃣ KNOWLEDGE GRAPH

**What is it?**
- Information stored as NODES (things) and LINKS (relationships)
- Everything is written as TRIPLES

**TRIPLE FORMAT:**
```
SUBJECT → PREDICATE → OBJECT
(Who?)  → (Does what?) → (To what?)

Example: John → teaches → Big Data
```

---

## 2️⃣ RDF (Resource Description Framework)

**What is it?**
- The LANGUAGE to write triples
- Every thing has a unique web address (IRI/URI)

**Key Points:**
- Subject = always an IRI (web address)
- Predicate = always an IRI
- Object = IRI OR literal (text/number)

**FORMATS:**
```
RDF/XML = complicated, lots of tags <...>
Turtle  = simple, like writing sentences
```

**CONTAINERS (for multiple items):**
```
rdf:Bag = unordered (shopping bag - order doesn't matter)
rdf:Seq = ordered (numbered list - order matters)
rdf:Alt = alternatives (pick ONE)
```

---

## 3️⃣ RDFS (RDF Schema)

**What is it?**
- Adds RULES to RDF
- Defines classes and properties

**KEY VOCABULARY:**
```
rdfs:Class      = a category of things
rdfs:subClassOf = "is a type of" (Dog subClassOf Animal)
rdfs:Property   = a relationship type
rdfs:domain     = WHO can use this property?
rdfs:range      = WHAT type is the result?
```

**DOMAIN & RANGE EXAMPLE:**
```
hasWife:
  domain = Man (only men can have wives)
  range = Woman (the wife must be a woman)
```

**INFERENCE:**
```
If: "knows" has domain Person
And: Alice knows Bob
Then: Alice IS A Person (computer figures this out!)
```

**LIMITATIONS of RDFS:**
- ❌ Can't say "exactly 2 parents"
- ❌ Can't say inverse (A married B → B married A)
- ❌ Can't say transitive (A > B > C → A > C)
- That's why we need OWL!

---

## 4️⃣ SKOS (Simple Knowledge Organization System)

**What is it?**
- For organizing VOCABULARY (like a thesaurus)
- NOT for data structure!

**KEY RELATIONSHIPS:**
```
skos:broader   = goes UP (Cat broader Animal)
skos:narrower  = goes DOWN (Animal narrower Cat)
skos:related   = sideways connection (Economics related Politics)
```

**COMMON MISTAKE:**
```
WRONG: UK rdfs:subClassOf Europe (says UK is TYPE of Europe)
RIGHT: UK skos:broader Europe (says UK is WITHIN Europe category)
```

**USE:**
- rdfs:subClassOf → for classes/types (Dog is a type of Animal)
- skos:broader → for vocabulary/concepts (UK is in Europe)

---

## 5️⃣ OWL (Web Ontology Language) ⭐ MOST IMPORTANT!

**What is it?**
- The MOST POWERFUL ontology language
- Can express complex rules

**ONTOLOGY = formal description of a domain with:**
```
1. Classes (categories)
2. Properties (relationships)
3. Constraints (rules)
4. Individuals (actual data)
```

**TBox vs ABox:**
```
TBox = the RULES/STRUCTURE (blueprint)
ABox = the ACTUAL DATA (filled-in form)
```

### OWL PROPERTY TYPES:

**Object Property** = links thing to thing
```
John → hasWife → Mary
```

**Data Property** = links thing to value
```
John → hasAge → "45"
```

### OWL PROPERTY CHARACTERISTICS:

```
owl:FunctionalProperty     = only ONE value (hasSSN)
owl:InverseFunctionalProperty = value points to ONE thing
owl:SymmetricProperty      = works both ways (isFriendOf)
owl:AsymmetricProperty     = only one way (isParentOf)
owl:TransitiveProperty     = chains (A>B, B>C → A>C)
owl:ReflexiveProperty      = applies to self (knows)
owl:IrreflexiveProperty    = can't apply to self
```

### OWL CLASS FEATURES:

```
owl:disjointWith    = can't be both (Man disjoint Woman)
owl:equivalentClass = same thing (Human = Person)
owl:inverseOf       = opposite relationship
```

**EXAMPLE:**
```
If: hasWife inverseOf hasHusband
And: John hasWife Mary
Then: Mary hasHusband John (automatic!)
```

---

## 6️⃣ REASONER

**What does it do?**
```
1. Consistency Checking = find contradictions
2. Classification = build complete hierarchy
3. Realisation = find class of each individual
4. Inference = discover new facts
```

**Popular Reasoners:** HermiT, Pellet, FaCT++

---

## 7️⃣ PROTÉGÉ (The Tool)

**Steps to create ontology:**
```
1. Set IRI (unique web address)
2. Create classes (Person, Animal...)
3. Create hierarchy (Man subClassOf Person)
4. Add object properties (hasWife, teaches)
5. Add data properties (hasAge, hasName)
6. Set characteristics (symmetric, transitive...)
7. Add individuals (John, Mary)
8. Run reasoner → discover new facts!
```

---

## 📊 QUICK COMPARISON TABLE

| Feature | RDF | RDFS | SKOS | OWL |
|---------|-----|------|------|-----|
| Purpose | Store triples | Add basic rules | Organize vocabulary | Full ontology |
| Classes | No | Yes | Concepts | Yes + features |
| Hierarchy | No | subClassOf | broader/narrower | subClassOf + more |
| Inverse | No | No | No | Yes! |
| Symmetric | No | No | No | Yes! |
| Transitive | No | No | Yes (explicit) | Yes! |
| Disjoint | No | No | No | Yes! |
| Cardinality | No | No | No | Yes! |

---

## 🚨 EXAM TIPS

1. **Know the difference between:**
   - rdfs:subClassOf (for types) vs skos:broader (for vocabulary)
   - Object property (thing→thing) vs Data property (thing→value)
   - TBox (rules) vs ABox (data)

2. **Remember property characteristics:**
   - Symmetric = works both ways (friend)
   - Transitive = chains (ancestor)
   - Functional = only one value (SSN)
   - Inverse = opposite relationship (wife/husband)

3. **OWL is built ON TOP of RDF and RDFS!**

4. **A reasoner discovers facts you didn't explicitly state!**

---

## 🎓 ONE-LINE SUMMARIES

- **RDF:** How to write facts as triples
- **RDFS:** How to add basic rules to facts
- **SKOS:** How to organize vocabulary/concepts
- **OWL:** How to express complex knowledge with reasoning
- **Ontology:** A formal description of a domain
- **Reasoner:** Software that discovers hidden facts

---

Good luck on your exam! 🍀
