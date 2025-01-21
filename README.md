# Prisma Utilities - Personal Learning Project

This repository contains a collection of Prisma utilities that I have discovered and created during my personal learning journey. The project is constantly updated with new findings, improvements, and tools that I would use in my personal projects.

The utilities here are intended to simplify and enhance the development process when using Prisma ORM. As this is a personal project built from my own experiences, it is not publicly available, and it serves as a resource for my own projects.

Feel free to explore the code, but please note that it is not intended for public use or production-ready environments.

## Getting Started

To use the Prisma utilities in your own project, follow these steps:

### Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v14.x or newer)
- [Prisma ORM](https://www.prisma.io/docs/getting-started)

### Installation

1. Clone this repository to your local machine:

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Build the project:

   ```bash
   npm run build
   ```

### Importing into Your Project

To use the utilities in any other project, you can install the package directly from your local machine:

1. In your project folder, run the following command to install the utility package from the local repository:

   ```bash
   npm install <path-to-repository>
   ```

   For example:

   ```bash
   npm install /path/to/prisma-utils
   ```

2. Import the required utilities into your project:

   ```ts
   import { paginate } from 'prisma-utils';
   ```

### Usage

Once the package is imported, you can use the utilities in your project as needed. For example, the pagination utility can be used like this:

```ts
import { paginate } from 'prisma-utils';

const result = await paginate(
  prisma.modelName, // your Prisma model
  { page: 1, pageSize: 10 },
  { where: { status: 'active' } },
  { include: { user: true } },
  { orderBy: { createdAt: 'desc' } }
);

console.log(result);
```

### Running Tests (Optional)

If you want to run any tests associated with the utilities (if any):

1. Run the test command:

   ```bash
   npm test
   ```

## Contributing

This project is primarily for my personal use, so contributions are not actively accepted. However, feel free to explore and learn from the code!

---

This README provides clear instructions on how to set up and use your Prisma utilities repository in other projects. Let me know if you need any further adjustments! 😊
