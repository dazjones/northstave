# northstave.com - Personal Blog

## About

My blog northstave.com is a place where I share my thoughts, projects, and experiences. The blog is powered by Hugo, a fast and flexible static site generator.

## Getting Started

To set up a local version of the blog for development or contributions, follow these steps:

### Prerequisites

- [Git](https://git-scm.com/)
- [Hugo](https://gohugo.io/getting-started/installing/) (extended version recommended)

### Installation

1. **Clone the repository:**
   ```sh
   git clone ssh://git@git.tower.northstave.com/darren/northstave.com.git
   cd northstave.com
   git submodule update -i
   ```
2. **Install dependencies:**

    Ensure you have the Hugo extended version installed. For more details, visit Hugo's installation guide.

3. **Run the development server:**
```sh
hugo server
```
The site will be available at http://localhost:1313/.

## Deployment
The site is automatically deployed to Tower on the main branch. Simply push changes to this branch, and Forgejo Actions will handle the deployment.


## Acknowledgements

- [Hugo](https://gohugo.io/getting-started/installing/) - The static site generator used for this blog.

This README was last updated on April 26th, 2026.
