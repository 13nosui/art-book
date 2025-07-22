# System Architecture

## Project Structure

**Total Files:** 43
**Total Lines of Code:** 30,681

### Language Distribution


- **TypeScript:** 19 files (6,868 lines, 22.4%)

- **TypeScript React:** 8 files (778 lines, 2.5%)

- **JSON:** 5 files (20,057 lines, 65.4%)

- **JavaScript:** 5 files (811 lines, 2.6%)

- **Markdown:** 6 files (2,167 lines, 7.1%)


### Directory Structure


#### [fileId]
- **Path:** `src/app/api/figma/[fileId]`
- **Files:** 1
- **Subdirectories:** 0



#### figma
- **Path:** `src/app/api/figma`
- **Files:** 0
- **Subdirectories:** 1



#### api
- **Path:** `src/app/api`
- **Files:** 0
- **Subdirectories:** 1
- **Purpose:** API routes and endpoints


#### app
- **Path:** `src/app`
- **Files:** 5
- **Subdirectories:** 1
- **Purpose:** Next.js app directory structure


#### components
- **Path:** `src/components`
- **Files:** 2
- **Subdirectories:** 0
- **Purpose:** React components and UI elements


#### hooks
- **Path:** `src/hooks`
- **Files:** 1
- **Subdirectories:** 0
- **Purpose:** Custom React hooks


#### lib
- **Path:** `src/lib`
- **Files:** 10
- **Subdirectories:** 0
- **Purpose:** Utility libraries and helper functions


#### api
- **Path:** `src/pages/api`
- **Files:** 1
- **Subdirectories:** 0
- **Purpose:** API routes and endpoints


#### pages
- **Path:** `src/pages`
- **Files:** 0
- **Subdirectories:** 1
- **Purpose:** Next.js pages and routing


#### stories
- **Path:** `src/stories`
- **Files:** 1
- **Subdirectories:** 0
- **Purpose:** Storybook stories


#### types
- **Path:** `src/types`
- **Files:** 1
- **Subdirectories:** 0
- **Purpose:** TypeScript type definitions


#### src
- **Path:** `src`
- **Files:** 0
- **Subdirectories:** 7



## Architectural Patterns

**Detected Patterns:** 2


### Provider Pattern

**Description:** React Context providers for state management
**Confidence:** 90%
**Files:** 4

**Examples:**
- `src/lib/auth-context.tsx`
- `src/app/providers.tsx`
- `kiro/src/lib/auth-context.tsx`

---

### Custom Hooks Pattern

**Description:** Reusable stateful logic with custom React hooks
**Confidence:** 95%
**Files:** 2

**Examples:**
- `src/hooks/useFigmaAPI.ts`
- `kiro/src/hooks/useFigmaAPI.ts`

