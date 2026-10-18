marketplace/                              - Marketplace platform repository
│
├── README.md                             - Project overview and setup guide
├── AGENTS.md                             - Shared engineering rules for AI agents
├── CLAUDE.md                             - Loads shared rules for Claude Code
├── package.json                          - Project commands and dependencies
├── pnpm-workspace.yaml                   - Connects apps and shared packages
├── pnpm-lock.yaml                        - Locks dependency versions
├── .env.example                          - Configuration template without secrets
├── .gitignore                            - Excludes secrets and generated files
├── .mcp.json                             - Optional approved tool connections
│
├── .claude/                              - AI development configuration
│   │
│   ├── settings.json                     - Permissions and hook configuration
│   ├── settings.local.json               - Personal settings; excluded from Git
│   │
│   ├── rules/                            - Standards for specific code areas
│   │   ├── backend.md                    - API and business-logic standards
│   │   ├── frontend.md                   - UI and accessibility standards
│   │   ├── database.md                   - Schema and migration standards
│   │   └── security.md                   - Access-control and data-handling rules
│   │
│   ├── agents/                           - Specialist reviewers used when needed
│   │   ├── code-reviewer.md               - Reviews correctness and regressions
│   │   ├── security-reviewer.md           - Reviews access and payment risks
│   │   └── database-reviewer.md           - Reviews migrations and data integrity
│   │
│   ├── skills/                           - Reusable development workflows
│   │   ├── plan-feature/SKILL.md          - Plans scope and acceptance criteria
│   │   ├── verify-change/SKILL.md         - Runs checks and records results
│   │   └── prepare-release/SKILL.md       - Prepares rollout and recovery steps
│   │
│   └── hooks/                            - Scripts registered in settings.json
│       ├── check-tool-action.mjs         - Checks configured tool actions
│       └── format-changed-files.mjs      - Formats supported edited files
│
├── docs/                                 - Shared product and engineering knowledge
│   │
│   ├── index.md                          - Documentation guide for people and agents
│   │
│   ├── product/                          - Business requirements
│   │   ├── requirements.md               - Features, scope, and expected outcomes
│   │   └── roles-and-permissions.md       - Buyer, seller, and admin access
│   │
│   ├── architecture/                     - System design
│   │   ├── overview.md                   - Components and system boundaries
│   │   └── decisions/                    - Key decisions and their reasons
│   │
│   ├── domain/                           - Core business rules
│   │   ├── orders.md                     - Delivery, revisions, and cancellation
│   │   ├── payments.md                   - Charges, fees, refunds, and payouts
│   │   └── reviews.md                    - Review eligibility and moderation
│   │
│   ├── features/                         - Specifications for individual features
│   │
│   └── runbooks/                         - Operating and recovery procedures
│       ├── deployment.md                 - Staging and production release steps
│       ├── rollback.md                   - Recovery from a failed release
│       ├── backup-recovery.md            - Database backup and restore steps
│       └── incident-response.md          - Incident ownership and response
│
├── apps/                                 - Applications that run the marketplace
│   │
│   ├── web/                              - Buyer, seller, and admin interfaces
│   │
│   ├── api/src/modules/                  - Backend business capabilities
│   │   ├── identity/                     - Accounts, roles, and authorization
│   │   ├── catalog/                      - Categories, listings, and packages
│   │   ├── orders/                       - Purchases, milestones, and delivery
│   │   ├── payments/                     - Payments, refunds, and payout records
│   │   ├── messaging/                    - Conversations and attachments
│   │   ├── reviews/                      - Ratings and verified feedback
│   │   ├── notifications/                - Notification preferences and delivery
│   │   └── moderation/                   - Reports, disputes, and admin actions
│   │
│   └── worker/                           - Background jobs and queued processing
│
├── packages/                             - Shared code used by applications
│   ├── db/                               - Database schema, migrations, and seeds
│   ├── contracts/                        - Shared API schemas and types
│   └── ui/                               - Reusable interface components
│
├── tests/                                - Verification across the platform
│   ├── integration/                      - API, database, and integration checks
│   └── e2e/                              - Complete buyer and seller journeys
│
├── infra/                                - Infrastructure and operational setup
│   ├── environments/                     - Staging and production definitions
│   └── observability/                    - Logging, monitoring, and alerts
│
├── scripts/                              - Repeatable engineering utilities
│   ├── setup.mjs                         - Prepares local development
│   └── verify.mjs                        - Runs agreed verification checks
│
└── .github/                              - Team review and release automation
    ├── CODEOWNERS                        - Defines review ownership
    ├── pull_request_template.md          - Records changes, tests, and risks
    └── workflows/
        ├── ci.yml                        - Runs automated pull-request checks
        └── deploy.yml                    - Runs controlled deployments
