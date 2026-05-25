## Outline Template

### Venue-Aware Notes
- Use this template for IEEE Wireless Communications Letters style submissions.
- Keep the main body within 4500 words.
- Keep figures and tables within 6 total.
- Avoid formulas unless necessary; never plan more than 3 simple formulas.
- Merge related work into the Introduction unless a standalone section is indispensable.
- Every section should end with a sentence that naturally opens the next section.

### JSON
{
  "outline_id": "wcl-outline-001",
  "topic": "",
  "venue": "IEEE Wireless Communications Letters",
  "story_arc": [
    "motivation",
    "gap",
    "method",
    "evidence",
    "implication"
  ],
  "global_constraints": {
    "body_word_limit": 4500,
    "target_body_words": [3600, 4300],
    "max_figures_tables_total": 6,
    "preferred_reference_limit": 15,
    "max_equations": 3,
    "language_rule": "If Chinese source material is used, rewrite into idiomatic academic English.",
    "flow_rule": "Each paragraph should hand off one keyword, tension, or implication to the next paragraph."
  },
  "core_points": [
    "Practical wireless problem",
    "Precise technical gap",
    "Method or framework",
    "Quantitative evidence",
    "Deployment implication"
  ],
  "structure": [
    {
      "section_id": "sec-abs",
      "title": "Abstract",
      "paragraph_range": { "min": 1, "max": 1 },
      "word_range": { "min": 120, "max": 180 },
      "paragraphs": [
        {
          "paragraph_id": "abs-1",
          "thesis": "Context, gap, proposed method, key result, and significance in one compact paragraph.",
          "evidence_type": "claim_summary",
          "word_range": { "min": 120, "max": 180 },
          "definition_of_done": [
            "Must define the problem setting in the first two sentences.",
            "Must state what is proposed or investigated.",
            "Must report at least one concrete outcome or observed gain.",
            "Must avoid citations, equations, and undefined acronyms."
          ]
        }
      ]
    },
    {
      "section_id": "sec-1",
      "title": "Introduction",
      "core_points": [
        "application or system motivation",
        "limitation of current practice",
        "specific gap",
        "contribution summary"
      ],
      "paragraph_range": { "min": 3, "max": 5 },
      "word_range": { "min": 700, "max": 1000 },
      "paragraphs": [
        {
          "paragraph_id": "p-1",
          "thesis": "Establish the wireless problem and why it matters now.",
          "evidence_type": "motivation_with_citations",
          "word_range": { "min": 160, "max": 240 },
          "definition_of_done": [
            "Must begin with a concrete wireless context, not a generic technology slogan.",
            "Must define the central concept or scenario by the end of the paragraph.",
            "Last sentence must set up the current limitation."
          ]
        },
        {
          "paragraph_id": "p-2",
          "thesis": "Explain why existing approaches are inadequate.",
          "evidence_type": "baseline_gap",
          "word_range": { "min": 160, "max": 220 },
          "definition_of_done": [
            "Must name the strongest relevant baseline family.",
            "Must explain the failure mode under this paper's operating conditions.",
            "Last sentence must motivate the proposed direction."
          ]
        },
        {
          "paragraph_id": "p-3",
          "thesis": "State the paper's core idea and contributions.",
          "evidence_type": "contribution_statement",
          "word_range": { "min": 140, "max": 220 },
          "definition_of_done": [
            "Must summarize the method in plain technical English.",
            "Must state 2-4 concrete contributions or findings.",
            "Must avoid inflated novelty language."
          ]
        }
      ]
    },
    {
      "section_id": "sec-2",
      "title": "System Model / Problem Formulation",
      "core_points": [
        "scenario",
        "assumptions",
        "notation economy",
        "optimization target or estimation target"
      ],
      "paragraph_range": { "min": 2, "max": 4 },
      "word_range": { "min": 500, "max": 800 },
      "paragraphs": [
        {
          "paragraph_id": "p-4",
          "thesis": "Define the system setup and symbols with minimal overhead.",
          "evidence_type": "problem_setup",
          "word_range": { "min": 220, "max": 320 },
          "definition_of_done": [
            "Must introduce only notation used later.",
            "If equations appear, they must be simple and intuitively explained.",
            "Must connect the setup to the difficulty introduced in the Introduction."
          ]
        },
        {
          "paragraph_id": "p-5",
          "thesis": "Formalize the task or objective and expose the core technical bottleneck.",
          "evidence_type": "objective_and_bottleneck",
          "word_range": { "min": 180, "max": 280 },
          "definition_of_done": [
            "Must state what is estimated, optimized, predicted, or reconstructed.",
            "Must make the bottleneck explicit in one sentence.",
            "Last sentence must open the method section."
          ]
        }
      ]
    },
    {
      "section_id": "sec-3",
      "title": "Proposed Method / Framework",
      "core_points": [
        "design rationale",
        "algorithm or pipeline",
        "complexity or robustness note"
      ],
      "paragraph_range": { "min": 3, "max": 5 },
      "word_range": { "min": 900, "max": 1300 },
      "paragraphs": [
        {
          "paragraph_id": "p-6",
          "thesis": "Present the design intuition before implementation details.",
          "evidence_type": "intuition",
          "word_range": { "min": 180, "max": 260 },
          "definition_of_done": [
            "Must explain why the proposed method addresses the bottleneck.",
            "Must avoid jumping directly into equations or pseudo-code.",
            "Should prepare the reader for the pipeline or algorithm steps."
          ]
        },
        {
          "paragraph_id": "p-7",
          "thesis": "Describe the pipeline, architecture, or estimator in a reproducible order.",
          "evidence_type": "method_detail",
          "word_range": { "min": 260, "max": 420 },
          "definition_of_done": [
            "Must follow a stable order such as input -> processing -> output.",
            "Must define all intermediate objects used in later experiments.",
            "If a figure is used, the paragraph must explain what question the figure answers."
          ]
        },
        {
          "paragraph_id": "p-8",
          "thesis": "Clarify complexity, robustness, or deployment tradeoffs.",
          "evidence_type": "tradeoff_analysis",
          "word_range": { "min": 180, "max": 260 },
          "definition_of_done": [
            "Must state at least one cost, assumption, or limitation.",
            "Must link the tradeoff to practical wireless deployment.",
            "Last sentence must point to evaluation."
          ]
        }
      ]
    },
    {
      "section_id": "sec-4",
      "title": "Results and Discussion",
      "core_points": [
        "baseline comparison",
        "key numerical trend",
        "condition under which the gain appears",
        "engineering implication"
      ],
      "paragraph_range": { "min": 3, "max": 5 },
      "word_range": { "min": 900, "max": 1300 },
      "paragraphs": [
        {
          "paragraph_id": "p-9",
          "thesis": "State the evaluation setup and comparison baselines.",
          "evidence_type": "experiment_setup",
          "word_range": { "min": 180, "max": 260 },
          "definition_of_done": [
            "Must name baselines and fairness conditions.",
            "Must avoid excessive simulator detail unrelated to the claim.",
            "Last sentence should frame the first result."
          ]
        },
        {
          "paragraph_id": "p-10",
          "thesis": "Report the main result and interpret it.",
          "evidence_type": "main_result",
          "word_range": { "min": 220, "max": 320 },
          "definition_of_done": [
            "Must quantify the key gain or loss.",
            "Must explain why the trend occurs.",
            "Must connect the result to the method mechanism, not only the figure."
          ]
        },
        {
          "paragraph_id": "p-11",
          "thesis": "Probe robustness, ablation, or sensitivity.",
          "evidence_type": "secondary_result",
          "word_range": { "min": 180, "max": 280 },
          "definition_of_done": [
            "Must show when the method weakens or strengthens.",
            "Must identify at least one practical operating condition.",
            "Last sentence must prepare the conclusion."
          ]
        }
      ]
    },
    {
      "section_id": "sec-5",
      "title": "Conclusion",
      "core_points": [
        "what was solved",
        "what was learned",
        "where it applies"
      ],
      "paragraph_range": { "min": 1, "max": 2 },
      "word_range": { "min": 180, "max": 320 },
      "paragraphs": [
        {
          "paragraph_id": "p-12",
          "thesis": "Close the letter by restating the contribution, key result, and scope.",
          "evidence_type": "takeaway",
          "word_range": { "min": 180, "max": 320 },
          "definition_of_done": [
            "Must restate the contribution in one sentence different from the abstract wording.",
            "Must summarize the main evidence without repeating numbers mechanically.",
            "Must end with a grounded implication or next-step direction."
          ]
        }
      ]
    }
  ]
}

### YAML
outline_id: wcl-outline-001
topic: ""
venue: IEEE Wireless Communications Letters
story_arc:
  - motivation
  - gap
  - method
  - evidence
  - implication
global_constraints:
  body_word_limit: 4500
  target_body_words:
    - 3600
    - 4300
  max_figures_tables_total: 6
  preferred_reference_limit: 15
  max_equations: 3
  language_rule: If Chinese source material is used, rewrite it into idiomatic academic English.
  flow_rule: Each paragraph should hand off one keyword, tension, or implication to the next paragraph.
core_points:
  - Practical wireless problem
  - Precise technical gap
  - Method or framework
  - Quantitative evidence
  - Deployment implication
structure:
  - section_id: sec-1
    title: Introduction
    core_points:
      - application or system motivation
      - limitation of current practice
      - specific gap
      - contribution summary
    paragraph_range:
      min: 3
      max: 5
    word_range:
      min: 700
      max: 1000
  - section_id: sec-2
    title: System Model / Problem Formulation
    core_points:
      - scenario
      - assumptions
      - notation economy
      - optimization target or estimation target
    paragraph_range:
      min: 2
      max: 4
    word_range:
      min: 500
      max: 800
  - section_id: sec-3
    title: Proposed Method / Framework
    core_points:
      - design rationale
      - algorithm or pipeline
      - complexity or robustness note
    paragraph_range:
      min: 3
      max: 5
    word_range:
      min: 900
      max: 1300
  - section_id: sec-4
    title: Results and Discussion
    core_points:
      - baseline comparison
      - key numerical trend
      - operating condition
      - engineering implication
    paragraph_range:
      min: 3
      max: 5
    word_range:
      min: 900
      max: 1300
  - section_id: sec-5
    title: Conclusion
    core_points:
      - what was solved
      - what was learned
      - where it applies
    paragraph_range:
      min: 1
      max: 2
    word_range:
      min: 180
      max: 320