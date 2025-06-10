# Tech Docs Template

<!-- =========================================================
BACKEND API & DB SPEC • ENHANCED TEMPLATE (with change tracking)
Replace every <PLACEHOLDER>.

COMPLEXITY GUIDE

**Simple Feature**: Use basic template sections
**Real-time System**: Include WebSocket, pub/sub, connection management
**Distributed System**: Add load balancing, service coordination, scaling
**Enterprise System**: Include all above + security, monitoring, optimization

Remove this header on real specs
========================================================= -->

## 

## 📋 Summary of Changes

### New APIs

- `<new-endpoint-path>` - <description>

### Modifying Existing APIs

- 🚧 `<existing-endpoint-path>` - <description of changes>

### New Database Components

- 🆕 **Table**: `<table_name>` - <description>
- 🆕 **Field**: `<table.field>` - <description>

### Enhanced Features

- 🆕 <feature> - <description>

## 1 API DESIGN

<!-- For MODIFIED endpoints, use this enhanced format -->

### 🔗 Endpoint <n>: <Name> (Modified)

| Key | Value |
| --- | --- |
| Path | `<HTTP path>` |
| Method | <HTTP method> |
| Auth | Bearer JWT |
| Description | <description with changes highlighted> |

### 1.1 Request

```json
{
  "<existing_field>": "<example>",
  "<new_field>": "<example>" // 🆕 comment for new fields
}

```

| Field | Type | Required | New Field | Validation / Format | Description |
| --- | --- | --- | --- | --- | --- |
| <existing_field> | <type> | <Yes/No> | No | <format> | <existing description> |
| <new_field> | <type> | <Yes/No> | **Yes** | <format> | <new field description> |

### 1.2 Success (200)

```json
{
  "existing_response": "...",
  "new_response_field": "..." // 🆕 if applicable
}

```

### 1.3 Error Responses

| Status | Code | Message | Condition | New Error |
| --- | --- | --- | --- | --- |
| 400 | <EXISTING_CODE> | <msg> | <condition> | No |
| 400 | <NEW_CODE> | <msg> | <condition> | **Yes** |

<!-- For NEW endpoints, use this standard format -->

### 🔗 Endpoint <n>: <Name> (New)

| Key | Value |
| --- | --- |
| Path | `<HTTP path>` |
| Method | <HTTP method> |
| Auth | Bearer JWT |
| Description | <description> |

### 1.1 Request

```json
{ "<field>": "<example>" }

```

| Field | Type | Required | Validation / Format | Description |
| --- | --- | --- | --- | --- |
| <field> | <type> | <Yes/No> | <format> | <description> |

### 1.2 Success (200)

```json
{ "data": { … }, "meta": { … } }

```

### 1.3 Error Responses

| Status | Code | Message | Condition |
| --- | --- | --- | --- |
| 400 | <CODE> | <msg> | <condition> |

## 2 DATABASE SCHEMA

### 2.1 ER Diagram

```json
erDiagram
  EXISTING_TABLE ||--o{ NEW_TABLE : "relationship [NEW TABLE]"
  EXISTING_TABLE ||--o{ EXISTING_TABLE2 : "existing relationship"

  EXISTING_TABLE {
    id UUID PK
    existing_field string
    new_field string "[NEW FIELD]"
  }

  NEW_TABLE {
    id UUID PK "[NEW TABLE]"
    field1 string "[NEW TABLE]"
    field2 int "[NEW TABLE]"
  }

```

### 2.2 Schema Changes Summary

### New Tables

**Table: `<new_table_name>`**

| Column | Type | Description | New |
| --- | --- | --- | --- |
| id | BIGSERIAL PRIMARY KEY | Unique identifier | **Yes** |
| <field1> | <type> | <description> | **Yes** |

### Modified Tables

**Table: `<existing_table_name>`**

| Column | Type | Description | New Field |
| --- | --- | --- | --- |
| <existing_field> | <type> | <existing description> | No |
| <new_field> | <type> | <new field description> | **Yes** |

### 2.3 SQL Scripts

```sql
-- New table creation
CREATE TABLE <new_table> (
  id BIGSERIAL PRIMARY KEY,
  <field1> <type>,
  created_at TIMESTAMP DEFAULT NOW()
);

-- Existing table modifications
ALTER TABLE <existing_table> ADD COLUMN <new_field> <type>;

-- Create indexes
CREATE INDEX idx_<table>_<field> ON <table>(<field>);

```

## 3 REQUEST FLOW DIAGRAM

```json
sequenceDiagram
  participant Client
  participant API
  participant DB
  participant External

  Client ->> API : <HTTP method> /<path>
  API ->> DB : <SQL operation>
  API ->> External : <external call if applicable>
  External -->> API : <response>
  DB -->> API : <result>
  API -->> Client : 200 OK

```

## 4 IMPLEMENTATION DETAILS

### 4.1 Modified Files

- **<file_path>** - <description of changes>

### 4.2 New Files

- **<file_path>** - <description>

### 4.3 Configuration Changes

- <config change 1>
- <config change 2>

---

<!-- =========================================================
TEMPLATE USAGE INSTRUCTIONS
Remove this section in actual specifications
========================================================= -->

## 📝 Template Usage Guide

### When to Use This Template

✅ API & Database specifications

✅ Feature documentation with change tracking
✅ Technical specs for team collaboration
✅ GitHub-stored documentation

### Key Features

- **📋 Change Summary** - Overview of new vs modified components
- **🔧 Enhanced API Tables** - "New Field" columns for modifications
- **📊 Annotated ER Diagrams** - [NEW TABLE]/[NEW FIELD] markers
- **📝 Implementation Details** - File changes and configurations

### Formatting Rules

1. Use proper markdown table syntax with pipes `|`
2. Include table headers with alignment `|---|---|`
3. Mark new fields/components with **bold Yes**
4. Use 🚧 emoji for modified endpoints
5. Add [NEW TABLE]/[NEW FIELD] annotations in ER diagrams
6. Include implementation file changes

### Quality Checklist

- [ ]  All tables have proper markdown formatting
- [ ]  New vs existing components are clearly marked
- [ ]  ER diagram shows relationships and annotations
- [ ]  Implementation details include file changes
- [ ]  Code blocks use proper syntax highlighting
