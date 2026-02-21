# MEX Form Progress: Job Attendees

## Status
- **Phase**: Initialized
- **Last Updated**: 2026-02-21
- **Last Agent**: mex-init-agent
- **Current Feature**: None (initialization complete)

## Requirements
- **Form Name**: Job Attendees
- **defId**: JobAttendees
- **Description**: View and check in attendees for a job
- **Context Object**: Jobs
- **Form Type**: JSON-based form
- **Data Needs**: JobAllocations (with Resource reference) filtered by Job, Resources for static lookup
- **Key Interactions**: List page with attendee search, detail/edit page with check-in toggle, add/remove attendees, view contact details

## Design References
- **Figma Link**: None
- **Screenshots/Images**: None
- **External Links**: None
- **Original Requirements**: Display Attendees (JobAllocations) related to a job. Allow attendees to be checked in via a boolean toggle. Show contact details for each attendee: Name, Mobile Phone, Email, Category. Follow the JobProducts form pattern with list page + detail/edit page.

## Feature List

### Configuration (Foundation)
- [ ] F1: Configure upload_config.json with name "Job Attendees", defId "JobAttendees", engineVersion "1.0.0"
- [ ] F2: Configure metadata.json with contextObject "Jobs", references for JobAllocations->Resource
- [ ] F3: Set up locale file structure with en.json containing all attendee-related strings

### Data Layer
- [ ] F4: Define instanceFetch.json to query JobAllocations filtered by JobId, including Resource relationship fields (Name, MobilePhone, Email, Category, PrimaryPhone)
- [ ] F5: Define staticFetch.json to query all Resources for the attendee selection picker
- [ ] F6: Verify CheckedIn boolean field exists on JobAllocations (may need custom field -- document in Implementation Notes)

### Page Components
- [ ] F7: Create AttendeeListPage as list type page with sourceExpression "formData.JobAllocations"
- [ ] F8: Configure list page search filtering on Resource.Name and Resource.MobilePhone
- [ ] F9: Configure addNew action on list page to create new JobAllocation with default CheckedIn=false
- [ ] F10: Create UpsertAttendeePage as flat type page for attendee detail/edit

### View Components - List Page
- [ ] F11: Implement titleAndCaption item layout showing Resource.Name as title and MobilePhone as caption
- [ ] F12: Add color-coded tags showing "Checked In" (green) or "Not Checked In" (grey) based on CheckedIn field
- [ ] F13: Configure emptyText for when no attendees exist
- [ ] F14: Configure itemClickDestination to navigate to UpsertAttendeePage

### View Components - Detail/Edit Page
- [ ] F15: Add selectEditor for choosing a Resource (attendee) with search on Name, MobilePhone, Email
- [ ] F16: Add switchEditor for CheckedIn boolean toggle
- [ ] F17: Add Contact Details section with text_display components for Name, MobilePhone, Email, Category
- [ ] F18: Configure section visibility to only show Contact Details when a Resource is selected
- [ ] F19: Configure upsert with insert/update titles and button text
- [ ] F20: Configure delete action with confirmation dialog for removing attendees
- [ ] F21: Configure saveDraft with askWhenBack=true

### Expressions & Bindings
- [ ] F22: Set up data binding expressions for all fields (pageData.ResourceId, pageData.CheckedIn, pageData.Resource.*)
- [ ] F23: Configure Resource select page with itemTitle and itemCaption expressions
- [ ] F24: Add validator on ResourceId requiring an attendee to be selected

### Localization
- [ ] F25: Add all AttendeeListPage text keys to en.json (Title, ItemTitle, ItemCaption, Empty, Add, SearchPlaceholder, tags)
- [ ] F26: Add all UpsertAttendeePage text keys to en.json (titles, labels, buttons, delete confirmation, validation messages)
- [ ] F27: Add all ResourceSelectPage text keys to en.json (Title, ItemTitle, ItemCaption, Empty)

### Polish
- [ ] F28: Verify all locale binding expressions match en.json keys
- [ ] F29: Test list page empty state and search functionality
- [ ] F30: Test add/edit/delete flow end-to-end
- [ ] F31: Validate check-in toggle persists correctly on save

## Completed Features
[Features move here when done]

## Current Session
- **Feature**: None
- **Started**: N/A
- **Status**: Initialization complete

## Implementation Notes
- **Data Model Decision**: Using JobAllocations as the junction object between Jobs and Resources. Each JobAllocation has a ResourceId that references a Resource record with contact details (Name, MobilePhone, Email, Category).
- **CheckedIn Field**: The CheckedIn boolean field on JobAllocations may be a custom field that needs to be created in the Skedulo schema. If it does not exist, the coding agent should either: (a) use an existing boolean field on JobAllocations, or (b) note that a custom field needs to be provisioned.
- **Pattern Reference**: This form follows the exact same pattern as JobProducts -- list page with search and tags, detail/edit page with selectEditor + additional fields, add/update/delete CRUD operations.
- **Resource vs Contact**: Skedulo's standard model uses Resources (not Contacts) for job allocations. The Resource object contains Name, MobilePhone, Email, and Category fields that serve the attendee contact details requirement.

## Issues & Blockers
- The CheckedIn field on JobAllocations may need to be a custom field. Verify in the target Skedulo org before deployment.
- Resource.MobilePhone availability should be confirmed -- some orgs may use PrimaryPhone instead.

## Session Log
### Session 1: Initialization
- **Agent**: mex-init-agent
- **Date**: 2026-02-21
- **Actions**:
  - Analyzed JobProducts form as reference pattern
  - Designed data model using JobAllocations with Resource references
  - Rewrote all 6 MEX form files (upload_config, metadata, instanceFetch, staticFetch, ui_def, en.json)
  - Generated feature breakdown (31 features identified)
  - Created SPEC.md with progress tracking
  - Made initial commit
- **Features Created**: 31 total features across 7 categories
