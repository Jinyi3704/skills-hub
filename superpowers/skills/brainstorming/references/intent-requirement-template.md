# Intent Requirement Template

Use this reference when drafting an `意向需求说明书` or a similar formal requirement document.

## Purpose

- Use a formal, restrained, enterprise tone.
- Prefer implementation-ready wording over marketing language.
- Keep chapter numbering stable unless the user explicitly requests another format.
- Make the document self-contained and easy to hand off.

## When To Use This Template

Use this template by default for:

- business or cooperation intent requirements
- external platform or channel integration requirements
- early-stage requirement documents that need clear scope, process, and function inventory

If the user explicitly wants another template, follow the user instead.

For intent requirements, this template is the required final presentation format. Output should contain only confirmed content that can be written into the document.

## Recommended Title Styles

- `[项目名称]意向需求说明书`
- `[项目名称]需求说明书`
- `[项目名称]详细业务需求说明书`

If the user already gave a project title, preserve it and adjust only the suffix if needed.

## Recommended Structure

### 1 需求概述\*（A阶段）

#### 1.1 业务背景\*

请描述本次需求产生的背景和原因，简要说明该项目拟解决的问题，及表明本次需求的必要性和充分性；描述本次需求要达成的目标。

包含：业务、政策或合作背景，参与机构/部门/角色，预期业务目标。

#### 1.2 业务风险点分析\*

Describe:

- key business, operational, compliance, or process risks
- corresponding control measures or mitigation ideas

If there is no meaningful risk content, write `无`。用户可主动输入`无`表示该章节无内容。

### 2 功能需求\*（A阶段）

#### 2.1 主要业务场景及业务流程\*

Split the document by scenario. For each scenario, use:

- `2.1.x [场景名称]`
- `2.1.x.1 业务场景描述`
- `2.1.x.2 业务流程图`

For flow descriptions:

- write in actor-action form
- make validation, state changes, and response handling explicit
- prefer clear actors such as 企业用户、经办人员、综合前端、核心系统、监管平台、外部渠道

Recommended wording:

- 企业用户发起...
- 综合前端校验...
- 核心系统返回...
- 外部平台接收...

#### 2.2 功能清单\*

Include a function inventory table with these columns:

| 一级功能名称 | 二级功能名称 | 功能简介 | 补充说明 |
| ------------ | ------------ | -------- | -------- |
| 示例         | 示例         | 示例     | 示例     |

Column guidance:

- `一级功能名称`: capability group or module
- `二级功能名称`: concrete function, transaction, or interface
- `功能简介`: one-sentence summary of what the function does
- `补充说明`: defaults, constraints, prerequisites, exceptions, or boundary conditions

## Writing Rules

- Describe behavior in testable language.
- Make validations explicit.
- Make permissions explicit when relevant.
- Make interface inputs and outputs explicit when integration is involved.
- Prefer wording such as `当...时，系统应...` and `若...则不允许...`。
- Avoid vague phrasing such as `提升用户体验` unless the user explicitly wants that tone.

## Requirement Extraction Checklist

Clarify these before drafting:

- business background and objective
- participating roles and institutions
- upstream and downstream systems
- main scenarios and process flow
- input and output data
- rules, validations, permissions, and exception handling
- whether the document is for new build, optimization, intent alignment, or integration

If some information is not yet available:

- 用户可主动输入`无`表示该章节无内容或暂不需要填写
- 否则询问补充信息，不编造细节，不在文档中写入推测性placeholder

If a section required by this template cannot be truthfully completed with the current information and user did not input `无`, ask the user to supplement the missing content before finalizing the document.

## What Not To Do

- Do not reference local absolute file paths in the output.
- Do not hard-code real customer names unless the user explicitly wants them.
- Do not copy a private template verbatim into the skill.
- Do not leave key rules implicit when they affect implementation.
- Do not write uncertain content, guessed rules, or placeholder statements into the requirement body.
- Do not silently omit template-required sections because information is missing.
- **Do NOT consider or output sections not defined in this template** (e.g., 系统对接要求, 数据校验规则, 非功能性要求, 实施计划建议, 测试要求, 接口规范, 安全要求). Completely ignore these topics.

## Fallback Rule

If source material is incomplete, preserve at least:

1. `需求概述`
2. `功能需求`
3. `主要业务场景及业务流程`
4. `功能清单`

When used for intent-stage collection, keep the document concise, but still write only confirmed information.
