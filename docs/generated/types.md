# TypeScript Type Definitions

## Interfaces (98)


### ExtractedInterface

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 13
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `properties: InterfaceProperty[]`

- `extends?: string[]`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### InterfaceProperty

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 26
**Exported:** Yes



**Properties:**

- `name: string`

- `type: string`

- `optional: boolean`

- `documentation?: string`




---

### ExtractedType

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 33
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `definition: string`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### ExtractedEnum

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 45
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `members: EnumMember[]`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### EnumMember

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 57
**Exported:** Yes



**Properties:**

- `name: string`

- `value?: string | number`

- `documentation?: string`




---

### ExtractedFunction

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 63
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `parameters: FunctionParameter[]`

- `returnType: string`

- `exported: boolean`

- `async: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### FunctionParameter

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 77
**Exported:** Yes



**Properties:**

- `name: string`

- `type: string`

- `optional: boolean`

- `defaultValue?: string`




---

### ExtractedComponent

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 84
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `props?: ExtractedInterface`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### ExtractedHook

**File:** `kiro/scripts/doc-generation/ast-parser.ts`
**Line:** 96
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `parameters: FunctionParameter[]`

- `returnType: string`

- `dependencies: string[]`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### ProjectStructure

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 13
**Exported:** Yes



**Properties:**

- `directories: DirectoryInfo[]`

- `files: FileInfo[]`

- `totalFiles: number`

- `totalLines: number`

- `languages: LanguageStats[]`




---

### DirectoryInfo

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 21
**Exported:** Yes



**Properties:**

- `name: string`

- `path: string`

- `fileCount: number`

- `subdirectories: string[]`

- `purpose?: string`




---

### FileInfo

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 29
**Exported:** Yes



**Properties:**

- `name: string`

- `path: string`

- `extension: string`

- `size: number`

- `lines: number`

- `language: string`

- `imports: string[]`

- `exports: string[]`




---

### LanguageStats

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 40
**Exported:** Yes



**Properties:**

- `language: string`

- `fileCount: number`

- `lineCount: number`

- `percentage: number`




---

### DependencyGraph

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 47
**Exported:** Yes



**Properties:**

- `nodes: DependencyNode[]`

- `edges: DependencyEdge[]`




---

### DependencyNode

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 52
**Exported:** Yes



**Properties:**

- `id: string`

- `name: string`

- `type: "component" | "hook" | "utility" | "service" | "type"`

- `filePath: string`




---

### DependencyEdge

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 59
**Exported:** Yes



**Properties:**

- `from: string`

- `to: string`

- `type: "import" | "extends" | "implements" | "uses"`




---

### ArchitecturalPattern

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 65
**Exported:** Yes



**Properties:**

- `name: string`

- `description: string`

- `files: string[]`

- `confidence: number`

- `examples: string[]`




---

### SecurityPattern

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 73
**Exported:** Yes



**Properties:**

- `type: | "validation"
    | "sanitization"
    | "authentication"
    | "authorization"
    | "encryption"`

- `description: string`

- `files: string[]`

- `implementation: string`




---

### APIEndpoint

**File:** `kiro/scripts/doc-generation/code-analyzer.ts`
**Line:** 85
**Exported:** Yes



**Properties:**

- `method: string`

- `path: string`

- `filePath: string`

- `handler: string`

- `middleware: string[]`

- `authentication: boolean`

- `validation: boolean`

- `documentation?: string`




---

### DiagramConfig

**File:** `kiro/scripts/doc-generation/diagram-generator.ts`
**Line:** 23
**Exported:** Yes



**Properties:**

- `theme?: "default" | "dark" | "forest" | "neutral"`

- `direction?: "TB" | "TD" | "BT" | "RL" | "LR"`

- `maxNodes?: number`

- `includeExternal?: boolean`




---

### GenerationOptions

**File:** `kiro/scripts/generate-docs.ts`
**Line:** 16
**Exported:** No



**Properties:**

- `projectRoot?: string`

- `outputDir?: string`

- `generateDiagrams?: boolean`

- `verbose?: boolean`




---

### ValidationResult

**File:** `kiro/scripts/validate-docs.ts`
**Line:** 19
**Exported:** No



**Properties:**

- `file: string`

- `errors: string[]`

- `warnings: string[]`




---

### ValidationSummary

**File:** `kiro/scripts/validate-docs.ts`
**Line:** 25
**Exported:** No



**Properties:**

- `totalFiles: number`

- `validFiles: number`

- `filesWithErrors: number`

- `filesWithWarnings: number`

- `totalErrors: number`

- `totalWarnings: number`

- `results: ValidationResult[]`




---

### RequirementMapping

**File:** `kiro/scripts/validate-documentation-completeness.ts`
**Line:** 14
**Exported:** No



**Properties:**

- `id: string`

- `description: string`

- `documentationFiles: string[]`

- `status: "complete" | "partial" | "missing"`




---

### ValidationResult

**File:** `kiro/scripts/validate-documentation-completeness.ts`
**Line:** 21
**Exported:** No



**Properties:**

- `totalRequirements: number`

- `completedRequirements: number`

- `partialRequirements: number`

- `missingRequirements: number`

- `requirementMappings: RequirementMapping[]`

- `crossReferenceIssues: string[]`

- `missingDocumentation: string[]`




---

### ValidationError

**File:** `kiro/src/lib/validation.ts`
**Line:** 109
**Exported:** Yes



**Properties:**

- `field: string`

- `message: string`

- `code?: string`




---

### ValidationResult

**File:** `kiro/src/lib/validation.ts`
**Line:** 116
**Exported:** Yes



**Properties:**

- `success: boolean`

- `data?: T`

- `errors?: ValidationError[]`




---

### ApiClientConfig

**File:** `kiro/src/lib/api-client.ts`
**Line:** 33
**Exported:** Yes



**Properties:**

- `baseURL?: string`

- `timeout?: number`

- `retryAttempts?: number`

- `retryDelay?: number`

- `enableLogging?: boolean`

- `customHeaders?: Record<string, string>`

- `authConfig?: {
    type: 'bearer' | 'apikey' | 'custom';
    token?: string;
    apiKeyHeader?: string;
    customAuth?: (config: InternalAxiosRequestConfig) => InternalAxiosRequestConfig;
  }`




---

### ApiResponse

**File:** `kiro/src/lib/api-client.ts`
**Line:** 49
**Exported:** Yes



**Properties:**

- `data: T`

- `status: number`

- `message?: string`

- `timestamp: string`




---

### ApiError

**File:** `kiro/src/lib/api-client.ts`
**Line:** 57
**Exported:** Yes



**Properties:**

- `code: string`

- `message: string`

- `details?: unknown`

- `timestamp: string`

- `requestId?: string`




---

### RateLimitInfo

**File:** `kiro/src/lib/api-client.ts`
**Line:** 66
**Exported:** No



**Properties:**

- `remaining: number`

- `reset: number`

- `limit: number`




---

### FigmaFileResponse

**File:** `kiro/src/app/api/figma/[fileId]/route.ts`
**Line:** 7
**Exported:** No



**Properties:**

- `name: string`

- `lastModified: string`

- `version: string`

- `document?: {
    id: string;
    name: string;
    type: string;
  }`




---

### ErrorResponse

**File:** `kiro/src/app/api/figma/[fileId]/route.ts`
**Line:** 20
**Exported:** No



**Properties:**

- `error: string`

- `code?: string`

- `details?: unknown`

- `timestamp: string`

- `requestId?: string`




---

### FigmaData

**File:** `kiro/src/hooks/useFigmaAPI.ts`
**Line:** 5
**Exported:** No



**Properties:**

- `name: string`

- `lastModified: string`

- `version: string`

- `document?: {
    id: string;
    name: string;
    type: string;
  }`

- `metadata: {
    timestamp: string;
    requestId: string;
    status: string;
  }`




---

### ApiErrorInfo

**File:** `kiro/src/hooks/useFigmaAPI.ts`
**Line:** 22
**Exported:** No



**Properties:**

- `code: string`

- `message: string`

- `details?: unknown`

- `timestamp: string`

- `requestId?: string`




---

### UseFigmaAPIResult

**File:** `kiro/src/hooks/useFigmaAPI.ts`
**Line:** 31
**Exported:** No



**Properties:**

- `data: FigmaData | null`

- `loading: boolean`

- `error: ApiErrorInfo | null`

- `rateLimitInfo: {
    remaining: number;
    reset: number;
    limit: number;
  } | null`

- `fetchFigmaFile: (fileId: string, options?: FetchOptions) => Promise<void>`

- `clearError: () => void`

- `clearData: () => void`

- `retry: () => Promise<void>`




---

### FetchOptions

**File:** `kiro/src/hooks/useFigmaAPI.ts`
**Line:** 47
**Exported:** No



**Properties:**

- `useCache?: boolean`

- `timeout?: number`

- `skipValidation?: boolean`




---

### CacheEntry

**File:** `kiro/src/hooks/useFigmaAPI.ts`
**Line:** 54
**Exported:** No



**Properties:**

- `data: FigmaData`

- `timestamp: number`

- `expiry: number`




---

### NextResponseConstructor

**File:** `kiro/src/lib/cors-config.ts`
**Line:** 16
**Exported:** No



**Properties:**




---

### CorsConfig

**File:** `kiro/src/lib/cors-config.ts`
**Line:** 31
**Exported:** Yes



**Properties:**

- `allowedOrigins: string[] | string | ((origin: string) => boolean)`

- `allowedMethods: string[]`

- `allowedHeaders: string[]`

- `exposedHeaders?: string[]`

- `credentials?: boolean`

- `maxAge?: number`

- `preflightContinue?: boolean`

- `optionsSuccessStatus?: number`




---

### EnvironmentCorsConfig

**File:** `kiro/src/lib/cors-config.ts`
**Line:** 43
**Exported:** Yes



**Properties:**

- `development: CorsConfig`

- `staging: CorsConfig`

- `production: CorsConfig`




---

### EncryptedData

**File:** `kiro/src/lib/crypto.ts`
**Line:** 44
**Exported:** Yes

**Description:** 暗号化された結果の型定義


**Properties:**

- `encrypted: string`

- `iv: string`

- `salt: string`

- `tag: string`




---

### CSRFValidationResult

**File:** `kiro/src/lib/csrf.ts`
**Line:** 5
**Exported:** Yes



**Properties:**

- `isValid: boolean`

- `error?: string | undefined`




---

### CSRFTokenOptions

**File:** `kiro/src/lib/csrf.ts`
**Line:** 10
**Exported:** Yes



**Properties:**

- `cookieName?: string`

- `httpOnly?: boolean`

- `secure?: boolean`

- `sameSite?: 'strict' | 'lax' | 'none'`

- `maxAge?: number`

- `path?: string`




---

### CookieOptions

**File:** `kiro/src/lib/secure-storage.ts`
**Line:** 21
**Exported:** Yes



**Properties:**

- `maxAge?: number`

- `expires?: Date`

- `domain?: string`

- `path?: string`

- `secure?: boolean`

- `httpOnly?: boolean`

- `sameSite?: 'strict' | 'lax' | 'none'`




---

### ExtractedInterface

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 13
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `properties: InterfaceProperty[]`

- `extends?: string[]`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### InterfaceProperty

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 26
**Exported:** Yes



**Properties:**

- `name: string`

- `type: string`

- `optional: boolean`

- `documentation?: string`




---

### ExtractedType

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 33
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `definition: string`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### ExtractedEnum

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 45
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `members: EnumMember[]`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### EnumMember

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 57
**Exported:** Yes



**Properties:**

- `name: string`

- `value?: string | number`

- `documentation?: string`




---

### ExtractedFunction

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 63
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `parameters: FunctionParameter[]`

- `returnType: string`

- `exported: boolean`

- `async: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### FunctionParameter

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 77
**Exported:** Yes



**Properties:**

- `name: string`

- `type: string`

- `optional: boolean`

- `defaultValue?: string`




---

### ExtractedComponent

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 84
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `props?: ExtractedInterface`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### ExtractedHook

**File:** `scripts/doc-generation/ast-parser.ts`
**Line:** 96
**Exported:** Yes



**Properties:**

- `name: string`

- `filePath: string`

- `parameters: FunctionParameter[]`

- `returnType: string`

- `dependencies: string[]`

- `exported: boolean`

- `documentation?: string`

- `location: {
    line: number;
    column: number;
  }`




---

### ProjectStructure

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 13
**Exported:** Yes



**Properties:**

- `directories: DirectoryInfo[]`

- `files: FileInfo[]`

- `totalFiles: number`

- `totalLines: number`

- `languages: LanguageStats[]`




---

### DirectoryInfo

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 21
**Exported:** Yes



**Properties:**

- `name: string`

- `path: string`

- `fileCount: number`

- `subdirectories: string[]`

- `purpose?: string`




---

### FileInfo

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 29
**Exported:** Yes



**Properties:**

- `name: string`

- `path: string`

- `extension: string`

- `size: number`

- `lines: number`

- `language: string`

- `imports: string[]`

- `exports: string[]`




---

### LanguageStats

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 40
**Exported:** Yes



**Properties:**

- `language: string`

- `fileCount: number`

- `lineCount: number`

- `percentage: number`




---

### DependencyGraph

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 47
**Exported:** Yes



**Properties:**

- `nodes: DependencyNode[]`

- `edges: DependencyEdge[]`




---

### DependencyNode

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 52
**Exported:** Yes



**Properties:**

- `id: string`

- `name: string`

- `type: "component" | "hook" | "utility" | "service" | "type"`

- `filePath: string`




---

### DependencyEdge

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 59
**Exported:** Yes



**Properties:**

- `from: string`

- `to: string`

- `type: "import" | "extends" | "implements" | "uses"`




---

### ArchitecturalPattern

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 65
**Exported:** Yes



**Properties:**

- `name: string`

- `description: string`

- `files: string[]`

- `confidence: number`

- `examples: string[]`




---

### SecurityPattern

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 73
**Exported:** Yes



**Properties:**

- `type: | "validation"
    | "sanitization"
    | "authentication"
    | "authorization"
    | "encryption"`

- `description: string`

- `files: string[]`

- `implementation: string`




---

### APIEndpoint

**File:** `scripts/doc-generation/code-analyzer.ts`
**Line:** 85
**Exported:** Yes



**Properties:**

- `method: string`

- `path: string`

- `filePath: string`

- `handler: string`

- `middleware: string[]`

- `authentication: boolean`

- `validation: boolean`

- `documentation?: string`




---

### DiagramConfig

**File:** `scripts/doc-generation/diagram-generator.ts`
**Line:** 23
**Exported:** Yes



**Properties:**

- `theme?: "default" | "dark" | "forest" | "neutral"`

- `direction?: "TB" | "TD" | "BT" | "RL" | "LR"`

- `maxNodes?: number`

- `includeExternal?: boolean`




---

### GenerationOptions

**File:** `scripts/generate-docs.ts`
**Line:** 16
**Exported:** No



**Properties:**

- `projectRoot?: string`

- `outputDir?: string`

- `generateDiagrams?: boolean`

- `verbose?: boolean`




---

### ValidationResult

**File:** `scripts/validate-docs.ts`
**Line:** 19
**Exported:** No



**Properties:**

- `file: string`

- `errors: string[]`

- `warnings: string[]`




---

### ValidationSummary

**File:** `scripts/validate-docs.ts`
**Line:** 25
**Exported:** No



**Properties:**

- `totalFiles: number`

- `validFiles: number`

- `filesWithErrors: number`

- `filesWithWarnings: number`

- `totalErrors: number`

- `totalWarnings: number`

- `results: ValidationResult[]`




---

### RequirementMapping

**File:** `scripts/validate-documentation-completeness.ts`
**Line:** 14
**Exported:** No



**Properties:**

- `id: string`

- `description: string`

- `documentationFiles: string[]`

- `status: "complete" | "partial" | "missing"`




---

### ValidationResult

**File:** `scripts/validate-documentation-completeness.ts`
**Line:** 21
**Exported:** No



**Properties:**

- `totalRequirements: number`

- `completedRequirements: number`

- `partialRequirements: number`

- `missingRequirements: number`

- `requirementMappings: RequirementMapping[]`

- `crossReferenceIssues: string[]`

- `missingDocumentation: string[]`




---

### ValidationError

**File:** `src/lib/validation.ts`
**Line:** 109
**Exported:** Yes



**Properties:**

- `field: string`

- `message: string`

- `code?: string`




---

### ValidationResult

**File:** `src/lib/validation.ts`
**Line:** 116
**Exported:** Yes



**Properties:**

- `success: boolean`

- `data?: T`

- `errors?: ValidationError[]`




---

### ApiClientConfig

**File:** `src/lib/api-client.ts`
**Line:** 33
**Exported:** Yes



**Properties:**

- `baseURL?: string`

- `timeout?: number`

- `retryAttempts?: number`

- `retryDelay?: number`

- `enableLogging?: boolean`

- `customHeaders?: Record<string, string>`

- `authConfig?: {
    type: 'bearer' | 'apikey' | 'custom';
    token?: string;
    apiKeyHeader?: string;
    customAuth?: (config: InternalAxiosRequestConfig) => InternalAxiosRequestConfig;
  }`




---

### ApiResponse

**File:** `src/lib/api-client.ts`
**Line:** 49
**Exported:** Yes



**Properties:**

- `data: T`

- `status: number`

- `message?: string`

- `timestamp: string`




---

### ApiError

**File:** `src/lib/api-client.ts`
**Line:** 57
**Exported:** Yes



**Properties:**

- `code: string`

- `message: string`

- `details?: unknown`

- `timestamp: string`

- `requestId?: string`




---

### RateLimitInfo

**File:** `src/lib/api-client.ts`
**Line:** 66
**Exported:** No



**Properties:**

- `remaining: number`

- `reset: number`

- `limit: number`




---

### FigmaFileResponse

**File:** `src/app/api/figma/[fileId]/route.ts`
**Line:** 7
**Exported:** No



**Properties:**

- `name: string`

- `lastModified: string`

- `version: string`

- `document?: {
    id: string;
    name: string;
    type: string;
  }`




---

### ErrorResponse

**File:** `src/app/api/figma/[fileId]/route.ts`
**Line:** 20
**Exported:** No



**Properties:**

- `error: string`

- `code?: string`

- `details?: unknown`

- `timestamp: string`

- `requestId?: string`




---

### FigmaData

**File:** `src/hooks/useFigmaAPI.ts`
**Line:** 5
**Exported:** No



**Properties:**

- `name: string`

- `lastModified: string`

- `version: string`

- `document?: {
    id: string;
    name: string;
    type: string;
  }`

- `metadata: {
    timestamp: string;
    requestId: string;
    status: string;
  }`




---

### ApiErrorInfo

**File:** `src/hooks/useFigmaAPI.ts`
**Line:** 22
**Exported:** No



**Properties:**

- `code: string`

- `message: string`

- `details?: unknown`

- `timestamp: string`

- `requestId?: string`




---

### UseFigmaAPIResult

**File:** `src/hooks/useFigmaAPI.ts`
**Line:** 31
**Exported:** No



**Properties:**

- `data: FigmaData | null`

- `loading: boolean`

- `error: ApiErrorInfo | null`

- `rateLimitInfo: {
    remaining: number;
    reset: number;
    limit: number;
  } | null`

- `fetchFigmaFile: (fileId: string, options?: FetchOptions) => Promise<void>`

- `clearError: () => void`

- `clearData: () => void`

- `retry: () => Promise<void>`




---

### FetchOptions

**File:** `src/hooks/useFigmaAPI.ts`
**Line:** 47
**Exported:** No



**Properties:**

- `useCache?: boolean`

- `timeout?: number`

- `skipValidation?: boolean`




---

### CacheEntry

**File:** `src/hooks/useFigmaAPI.ts`
**Line:** 54
**Exported:** No



**Properties:**

- `data: FigmaData`

- `timestamp: number`

- `expiry: number`




---

### NextResponseConstructor

**File:** `src/lib/cors-config.ts`
**Line:** 16
**Exported:** No



**Properties:**




---

### CorsConfig

**File:** `src/lib/cors-config.ts`
**Line:** 31
**Exported:** Yes



**Properties:**

- `allowedOrigins: string[] | string | ((origin: string) => boolean)`

- `allowedMethods: string[]`

- `allowedHeaders: string[]`

- `exposedHeaders?: string[]`

- `credentials?: boolean`

- `maxAge?: number`

- `preflightContinue?: boolean`

- `optionsSuccessStatus?: number`




---

### EnvironmentCorsConfig

**File:** `src/lib/cors-config.ts`
**Line:** 43
**Exported:** Yes



**Properties:**

- `development: CorsConfig`

- `staging: CorsConfig`

- `production: CorsConfig`




---

### EncryptedData

**File:** `src/lib/crypto.ts`
**Line:** 44
**Exported:** Yes

**Description:** 暗号化された結果の型定義


**Properties:**

- `encrypted: string`

- `iv: string`

- `salt: string`

- `tag: string`




---

### CSRFValidationResult

**File:** `src/lib/csrf.ts`
**Line:** 5
**Exported:** Yes



**Properties:**

- `isValid: boolean`

- `error?: string | undefined`




---

### CSRFTokenOptions

**File:** `src/lib/csrf.ts`
**Line:** 10
**Exported:** Yes



**Properties:**

- `cookieName?: string`

- `httpOnly?: boolean`

- `secure?: boolean`

- `sameSite?: 'strict' | 'lax' | 'none'`

- `maxAge?: number`

- `path?: string`




---

### CookieOptions

**File:** `src/lib/secure-storage.ts`
**Line:** 21
**Exported:** Yes



**Properties:**

- `maxAge?: number`

- `expires?: Date`

- `domain?: string`

- `path?: string`

- `secure?: boolean`

- `httpOnly?: boolean`

- `sameSite?: 'strict' | 'lax' | 'none'`




---

### AuthContextType

**File:** `kiro/src/lib/auth-context.tsx`
**Line:** 7
**Exported:** No



**Properties:**

- `user: User | null`

- `loading: boolean`

- `error: string | null`

- `signOut: () => Promise<void>`




---

### AuthProviderProps

**File:** `kiro/src/lib/auth-context.tsx`
**Line:** 24
**Exported:** No



**Properties:**

- `children: ReactNode`




---

### AuthFormProps

**File:** `kiro/src/components/AuthForm.tsx`
**Line:** 12
**Exported:** No



**Properties:**

- `onSuccess?: () => void`




---

### PomodoroTimerProps

**File:** `kiro/src/components/PomodoroTimer.tsx`
**Line:** 7
**Exported:** No



**Properties:**

- `className?: string`




---

### AuthContextType

**File:** `src/lib/auth-context.tsx`
**Line:** 7
**Exported:** No



**Properties:**

- `user: User | null`

- `loading: boolean`

- `error: string | null`

- `signOut: () => Promise<void>`




---

### AuthProviderProps

**File:** `src/lib/auth-context.tsx`
**Line:** 24
**Exported:** No



**Properties:**

- `children: ReactNode`




---

### AuthFormProps

**File:** `src/components/AuthForm.tsx`
**Line:** 12
**Exported:** No



**Properties:**

- `onSuccess?: () => void`




---

### PomodoroTimerProps

**File:** `src/components/PomodoroTimer.tsx`
**Line:** 7
**Exported:** No



**Properties:**

- `className?: string`





## Type Aliases (20)


### ValidatorFunction

**File:** `kiro/src/lib/validation.ts`
**Line:** 199
**Exported:** Yes



```typescript
type ValidatorFunction = (data: unknown) => ValidationResult<T>;
```

---

### SchemaType

**File:** `kiro/src/lib/validation.ts`
**Line:** 200
**Exported:** Yes



```typescript
type SchemaType = T extends ValidatorFunction<infer U> ? U : never;
```

---

### FirebaseConfig

**File:** `kiro/src/lib/env.ts`
**Line:** 42
**Exported:** Yes

**Description:** Type definitions derived from schemas


```typescript
type FirebaseConfig = z.infer<typeof FirebaseConfigSchema>;
```

---

### AppConfig

**File:** `kiro/src/lib/env.ts`
**Line:** 43
**Exported:** Yes



```typescript
type AppConfig = z.infer<typeof AppConfigSchema>;
```

---

### EnvConfig

**File:** `kiro/src/lib/env.ts`
**Line:** 44
**Exported:** Yes



```typescript
type EnvConfig = z.infer<typeof EnvSchema>;
```

---

### NextRequest

**File:** `kiro/src/lib/cors-config.ts`
**Line:** 2
**Exported:** No



```typescript
type NextRequest = {
  method: string;
  headers: {
    get(name: string): string | null;
  };
};
```

---

### NextResponse

**File:** `kiro/src/lib/cors-config.ts`
**Line:** 9
**Exported:** No



```typescript
type NextResponse = {
  headers: {
    set(name: string, value: string): void;
  };
} & Response;
```

---

### SecurityLevel

**File:** `kiro/src/lib/cors-config.ts`
**Line:** 50
**Exported:** Yes



```typescript
type SecurityLevel = 'strict' | 'moderate' | 'permissive';
```

---

### StorageType

**File:** `kiro/src/lib/secure-storage.ts`
**Line:** 15
**Exported:** Yes

**Description:** 🔐 セキュアストレージユーティリティ

機密情報を暗号化してローカルストレージやセッションストレージに安全に保存します
ブラウザ環境とサーバー環境の両方をサポートします


```typescript
type StorageType = 'localStorage' | 'sessionStorage' | 'memory' | 'cookie';
```

---

### ValidatorFunction

**File:** `src/lib/validation.ts`
**Line:** 199
**Exported:** Yes



```typescript
type ValidatorFunction = (data: unknown) => ValidationResult<T>;
```

---

### SchemaType

**File:** `src/lib/validation.ts`
**Line:** 200
**Exported:** Yes



```typescript
type SchemaType = T extends ValidatorFunction<infer U> ? U : never;
```

---

### FirebaseConfig

**File:** `src/lib/env.ts`
**Line:** 42
**Exported:** Yes

**Description:** Type definitions derived from schemas


```typescript
type FirebaseConfig = z.infer<typeof FirebaseConfigSchema>;
```

---

### AppConfig

**File:** `src/lib/env.ts`
**Line:** 43
**Exported:** Yes



```typescript
type AppConfig = z.infer<typeof AppConfigSchema>;
```

---

### EnvConfig

**File:** `src/lib/env.ts`
**Line:** 44
**Exported:** Yes



```typescript
type EnvConfig = z.infer<typeof EnvSchema>;
```

---

### NextRequest

**File:** `src/lib/cors-config.ts`
**Line:** 2
**Exported:** No



```typescript
type NextRequest = {
  method: string;
  headers: {
    get(name: string): string | null;
  };
};
```

---

### NextResponse

**File:** `src/lib/cors-config.ts`
**Line:** 9
**Exported:** No



```typescript
type NextResponse = {
  headers: {
    set(name: string, value: string): void;
  };
} & Response;
```

---

### SecurityLevel

**File:** `src/lib/cors-config.ts`
**Line:** 50
**Exported:** Yes



```typescript
type SecurityLevel = 'strict' | 'moderate' | 'permissive';
```

---

### StorageType

**File:** `src/lib/secure-storage.ts`
**Line:** 15
**Exported:** Yes

**Description:** 🔐 セキュアストレージユーティリティ

機密情報を暗号化してローカルストレージやセッションストレージに安全に保存します
ブラウザ環境とサーバー環境の両方をサポートします


```typescript
type StorageType = 'localStorage' | 'sessionStorage' | 'memory' | 'cookie';
```

---

### Story

**File:** `kiro/src/stories/Example.stories.tsx`
**Line:** 33
**Exported:** No



```typescript
type Story = StoryObj<typeof meta>;
```

---

### Story

**File:** `src/stories/Example.stories.tsx`
**Line:** 33
**Exported:** No



```typescript
type Story = StoryObj<typeof meta>;
```


## Enums (0)


