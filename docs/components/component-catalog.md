# Component Catalog

This document provides a comprehensive catalog of all UI components available in the AI Development Template. These components are built using HeroUI and follow best practices for accessibility, performance, and design.

## Basic Components

### Button

The primary button component with multiple variants and sizes.

```tsx
import { Button } from "@heroui/react";

<Button variant="primary" size="md">
  Click Me
</Button>;
```

**Variants:**

- `primary` - Primary action button
- `secondary` - Secondary action button
- `outline` - Outlined button
- `ghost` - Ghost button
- `link` - Link button
- `destructive` - Destructive action button

**Sizes:**

- `sm` - Small button
- `md` - Medium button (default)
- `lg` - Large button
- `xl` - Extra large button

**Props:**

- `variant` - Button variant
- `size` - Button size
- `disabled` - Disable the button
- `loading` - Show loading state
- `onClick` - Click handler
- `className` - Additional CSS classes
- `children` - Button content

### Input

Text input component with various types and states.

```tsx
import { Input } from "@heroui/react";

<Input
  type="text"
  placeholder="Enter your name"
  value={name}
  onChange={(e) => setName(e.target.value)}
/>;
```

**Types:**

- `text` - Text input
- `password` - Password input
- `email` - Email input
- `number` - Number input
- `tel` - Telephone input
- `url` - URL input
- `search` - Search input

**Props:**

- `type` - Input type
- `placeholder` - Placeholder text
- `value` - Input value
- `onChange` - Change handler
- `disabled` - Disable the input
- `error` - Error message
- `className` - Additional CSS classes

### Card

Container component for grouping related content.

```tsx
import {
  Card,
  CardHeader,
  CardTitle,
  CardDescription,
  CardContent,
  CardFooter,
} from "@heroui/react";

<Card>
  <CardHeader>
    <CardTitle>Card Title</CardTitle>
    <CardDescription>Card description</CardDescription>
  </CardHeader>
  <CardContent>
    <p>Card content</p>
  </CardContent>
  <CardFooter>
    <p>Card footer</p>
  </CardFooter>
</Card>;
```

**Props:**

- `className` - Additional CSS classes
- `children` - Card content

### Select

Dropdown select component for selecting from a list of options.

```tsx
import {
  Select,
  SelectTrigger,
  SelectValue,
  SelectContent,
  SelectItem,
} from "@heroui/react";

<Select value={value} onValueChange={setValue}>
  <SelectTrigger>
    <SelectValue placeholder="Select an option" />
  </SelectTrigger>
  <SelectContent>
    <SelectItem value="option1">Option 1</SelectItem>
    <SelectItem value="option2">Option 2</SelectItem>
    <SelectItem value="option3">Option 3</SelectItem>
  </SelectContent>
</Select>;
```

**Props:**

- `value` - Selected value
- `onValueChange` - Value change handler
- `disabled` - Disable the select
- `className` - Additional CSS classes

### Checkbox

Checkbox component for boolean selections.

```tsx
import { Checkbox } from "@heroui/react";

<Checkbox checked={checked} onCheckedChange={setChecked} label="Remember me" />;
```

**Props:**

- `checked` - Checkbox state
- `onCheckedChange` - Change handler
- `label` - Checkbox label
- `disabled` - Disable the checkbox
- `className` - Additional CSS classes

### Radio

Radio button component for selecting one option from a group.

```tsx
import { RadioGroup, RadioGroupItem } from "@heroui/react";

<RadioGroup value={value} onValueChange={setValue}>
  <div className="flex items-center space-x-2">
    <RadioGroupItem value="option1" id="option1" />
    <label htmlFor="option1">Option 1</label>
  </div>
  <div className="flex items-center space-x-2">
    <RadioGroupItem value="option2" id="option2" />
    <label htmlFor="option2">Option 2</label>
  </div>
</RadioGroup>;
```

**Props:**

- `value` - Selected value
- `onValueChange` - Value change handler
- `disabled` - Disable the radio group
- `className` - Additional CSS classes

### Switch

Toggle switch component for boolean settings.

```tsx
import { Switch } from "@heroui/react";

<Switch
  checked={enabled}
  onCheckedChange={setEnabled}
  label="Enable notifications"
/>;
```

**Props:**

- `checked` - Switch state
- `onCheckedChange` - Change handler
- `label` - Switch label
- `disabled` - Disable the switch
- `className` - Additional CSS classes

### Textarea

Multi-line text input component.

```tsx
import { Textarea } from "@heroui/react";

<Textarea
  placeholder="Enter your message"
  value={message}
  onChange={(e) => setMessage(e.target.value)}
/>;
```

**Props:**

- `placeholder` - Placeholder text
- `value` - Textarea value
- `onChange` - Change handler
- `disabled` - Disable the textarea
- `error` - Error message
- `rows` - Number of rows
- `className` - Additional CSS classes

### Badge

Small status indicator component.

```tsx
import { Badge } from "@heroui/react";

<Badge variant="primary">New</Badge>;
```

**Variants:**

- `primary` - Primary badge
- `secondary` - Secondary badge
- `outline` - Outlined badge
- `destructive` - Destructive badge

**Props:**

- `variant` - Badge variant
- `className` - Additional CSS classes
- `children` - Badge content

### Avatar

User avatar component with fallback.

```tsx
import { Avatar, AvatarImage, AvatarFallback } from "@heroui/react";

<Avatar>
  <AvatarImage src="https://example.com/avatar.jpg" alt="User" />
  <AvatarFallback>JD</AvatarFallback>
</Avatar>;
```

**Props:**

- `className` - Additional CSS classes
- `children` - Avatar content

## Composite Components

### AuthForm

Authentication form component for login and registration.

```tsx
import { AuthForm } from "../components/AuthForm";

<AuthForm mode="login" onSuccess={handleSuccess} />;
```

**Props:**

- `mode` - Form mode: `login` or `register`
- `onSuccess` - Success callback
- `onError` - Error callback
- `className` - Additional CSS classes

### PomodoroTimer

Pomodoro timer component for productivity.

```tsx
import { PomodoroTimer } from "../components/PomodoroTimer";

<PomodoroTimer
  workDuration={25}
  breakDuration={5}
  onComplete={handleComplete}
/>;
```

**Props:**

- `workDuration` - Work duration in minutes
- `breakDuration` - Break duration in minutes
- `onComplete` - Completion callback
- `className` - Additional CSS classes

### FileUploader

File upload component with drag and drop support.

```tsx
import { FileUploader } from "../components/FileUploader";

<FileUploader
  accept="image/*"
  maxSize={5 * 1024 * 1024}
  onUpload={handleUpload}
/>;
```

**Props:**

- `accept` - Accepted file types
- `maxSize` - Maximum file size in bytes
- `onUpload` - Upload callback
- `multiple` - Allow multiple files
- `className` - Additional CSS classes

### DataTable

Table component for displaying and interacting with data.

```tsx
import { DataTable } from "../components/DataTable";

<DataTable columns={columns} data={data} pagination={true} sortable={true} />;
```

**Props:**

- `columns` - Table columns configuration
- `data` - Table data
- `pagination` - Enable pagination
- `sortable` - Enable sorting
- `filterable` - Enable filtering
- `className` - Additional CSS classes

## Layout Components

### Header

Application header component with navigation and user menu.

```tsx
import { Header } from "../components/Header";

<Header title="AI Development Template" user={user} onLogout={handleLogout} />;
```

**Props:**

- `title` - Application title
- `user` - User object
- `onLogout` - Logout callback
- `className` - Additional CSS classes

### Sidebar

Navigation sidebar component.

```tsx
import { Sidebar } from "../components/Sidebar";

<Sidebar
  items={navigationItems}
  collapsed={sidebarCollapsed}
  onToggle={toggleSidebar}
/>;
```

**Props:**

- `items` - Navigation items
- `collapsed` - Sidebar collapsed state
- `onToggle` - Toggle callback
- `className` - Additional CSS classes

### Footer

Application footer component.

```tsx
import { Footer } from "../components/Footer";

<Footer copyright="© 2025 Your Company" links={footerLinks} />;
```

**Props:**

- `copyright` - Copyright text
- `links` - Footer links
- `className` - Additional CSS classes

### Modal

Modal dialog component for displaying content on top of the page.

```tsx
import {
  Modal,
  ModalTrigger,
  ModalContent,
  ModalHeader,
  ModalTitle,
  ModalDescription,
  ModalFooter,
} from "@heroui/react";

<Modal>
  <ModalTrigger asChild>
    <Button>Open Modal</Button>
  </ModalTrigger>
  <ModalContent>
    <ModalHeader>
      <ModalTitle>Modal Title</ModalTitle>
      <ModalDescription>Modal description</ModalDescription>
    </ModalHeader>
    <div className="p-4">
      <p>Modal content</p>
    </div>
    <ModalFooter>
      <Button onClick={onClose}>Close</Button>
    </ModalFooter>
  </ModalContent>
</Modal>;
```

**Props:**

- `open` - Modal open state
- `onOpenChange` - Open state change handler
- `className` - Additional CSS classes
- `children` - Modal content

## Feedback Components

### Alert

Alert component for displaying messages.

```tsx
import { Alert, AlertTitle, AlertDescription } from "@heroui/react";

<Alert variant="info">
  <AlertTitle>Information</AlertTitle>
  <AlertDescription>This is an informational message.</AlertDescription>
</Alert>;
```

**Variants:**

- `default` - Default alert
- `info` - Informational alert
- `success` - Success alert
- `warning` - Warning alert
- `error` - Error alert

**Props:**

- `variant` - Alert variant
- `className` - Additional CSS classes
- `children` - Alert content

### Toast

Toast notification component for temporary messages.

```tsx
import { useToast } from "@heroui/react";

const { toast } = useToast();

toast({
  title: "Success",
  description: "Your changes have been saved.",
  variant: "success",
});
```

**Variants:**

- `default` - Default toast
- `info` - Informational toast
- `success` - Success toast
- `warning` - Warning toast
- `error` - Error toast

**Props:**

- `title` - Toast title
- `description` - Toast description
- `variant` - Toast variant
- `duration` - Toast duration in milliseconds
- `action` - Toast action button

### Progress

Progress indicator component.

```tsx
import { Progress } from "@heroui/react";

<Progress value={60} max={100} />;
```

**Props:**

- `value` - Current progress value
- `max` - Maximum progress value
- `className` - Additional CSS classes

### Skeleton

Skeleton loading component for content placeholders.

```tsx
import { Skeleton } from "@heroui/react";

<Skeleton className="h-12 w-full" />;
```

**Props:**

- `className` - Additional CSS classes

## Navigation Components

### Tabs

Tabbed interface component.

```tsx
import { Tabs, TabsList, TabsTrigger, TabsContent } from "@heroui/react";

<Tabs defaultValue="tab1">
  <TabsList>
    <TabsTrigger value="tab1">Tab 1</TabsTrigger>
    <TabsTrigger value="tab2">Tab 2</TabsTrigger>
  </TabsList>
  <TabsContent value="tab1">Tab 1 content</TabsContent>
  <TabsContent value="tab2">Tab 2 content</TabsContent>
</Tabs>;
```

**Props:**

- `defaultValue` - Default selected tab
- `value` - Selected tab
- `onValueChange` - Value change handler
- `className` - Additional CSS classes

### Breadcrumb

Breadcrumb navigation component.

```tsx
import {
  Breadcrumb,
  BreadcrumbItem,
  BreadcrumbLink,
  BreadcrumbSeparator,
} from "@heroui/react";

<Breadcrumb>
  <BreadcrumbItem>
    <BreadcrumbLink href="/">Home</BreadcrumbLink>
  </BreadcrumbItem>
  <BreadcrumbSeparator />
  <BreadcrumbItem>
    <BreadcrumbLink href="/products">Products</BreadcrumbLink>
  </BreadcrumbItem>
  <BreadcrumbSeparator />
  <BreadcrumbItem>
    <BreadcrumbLink>Product Name</BreadcrumbLink>
  </BreadcrumbItem>
</Breadcrumb>;
```

**Props:**

- `className` - Additional CSS classes
- `children` - Breadcrumb content

### Pagination

Pagination component for navigating through pages.

```tsx
import {
  Pagination,
  PaginationContent,
  PaginationItem,
  PaginationLink,
  PaginationNext,
  PaginationPrevious,
} from "@heroui/react";

<Pagination>
  <PaginationContent>
    <PaginationItem>
      <PaginationPrevious href="#" />
    </PaginationItem>
    <PaginationItem>
      <PaginationLink href="#">1</PaginationLink>
    </PaginationItem>
    <PaginationItem>
      <PaginationLink href="#" isActive>
        2
      </PaginationLink>
    </PaginationItem>
    <PaginationItem>
      <PaginationLink href="#">3</PaginationLink>
    </PaginationItem>
    <PaginationItem>
      <PaginationNext href="#" />
    </PaginationItem>
  </PaginationContent>
</Pagination>;
```

**Props:**

- `className` - Additional CSS classes
- `children` - Pagination content

## Form Components

### Form

Form component with validation.

```tsx
import {
  Form,
  FormField,
  FormItem,
  FormLabel,
  FormControl,
  FormDescription,
  FormMessage,
} from "@heroui/react";
import { useForm } from "react-hook-form";
import { z } from "zod";
import { zodResolver } from "@hookform/resolvers/zod";

const formSchema = z.object({
  username: z.string().min(2).max(50),
});

const form = useForm({
  resolver: zodResolver(formSchema),
  defaultValues: {
    username: "",
  },
});

<Form {...form}>
  <form onSubmit={form.handleSubmit(onSubmit)}>
    <FormField
      control={form.control}
      name="username"
      render={({ field }) => (
        <FormItem>
          <FormLabel>Username</FormLabel>
          <FormControl>
            <Input {...field} />
          </FormControl>
          <FormDescription>Enter your username</FormDescription>
          <FormMessage />
        </FormItem>
      )}
    />
    <Button type="submit">Submit</Button>
  </form>
</Form>;
```

**Props:**

- `className` - Additional CSS classes
- `children` - Form content

### Label

Form label component.

```tsx
import { Label } from "@heroui/react";

<Label htmlFor="email">Email</Label>;
```

**Props:**

- `htmlFor` - Associated form element ID
- `className` - Additional CSS classes
- `children` - Label content

### Slider

Range slider component.

```tsx
import { Slider } from "@heroui/react";

<Slider
  defaultValue={[50]}
  min={0}
  max={100}
  step={1}
  onValueChange={setValue}
/>;
```

**Props:**

- `defaultValue` - Default slider value
- `value` - Slider value
- `onValueChange` - Value change handler
- `min` - Minimum value
- `max` - Maximum value
- `step` - Step value
- `disabled` - Disable the slider
- `className` - Additional CSS classes

## Additional Resources

- [Generated Component Documentation](../generated/components.md) - Automatically generated component documentation
- [HeroUI Documentation](https://heroui.dev) - Official HeroUI documentation
