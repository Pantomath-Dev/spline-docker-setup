# Spline Docker Setup

This repository contains the Docker compose file for deploying the Spline Server.

## Deployment Instructions

When changes are made to this repository and need to be deployed, follow these steps:

1. **Create a New Git Tag**
   - Make sure your changes are merged into the `main` branch.
   - Create a new tag from `main` using the following Git command:
     ```bash
     git tag <new-version-tag>
     git push origin <new-version-tag>
     ```
   - Example:
     ```bash
     git tag 1.0.2
     git push origin 1.0.2i
     ```

2. **Update the Referenced URL in `iac-infrastructure`**
   - Navigate to the `iac-infrastructure` repository.
   - Locate the following line in the `customer-management-stack.ts` file:
     [Line 1642](https://github.com/Pantomath-Dev/iac-infrastructure/blob/df4df5b66c35a88bc3308823045e2e3749ed91b9/src/modules/customer-management/customer-management-stack.ts#L1642)
   - Update the URL to reference the new tag you just created. For example:
     
     ```bash
     wget https://raw.githubusercontent.com/Pantomath-Dev/spline-docker-setup/1.0.2/compose.yaml
     ```
   
## Notes

- Ensure all changes are thoroughly tested before tagging.
- Follow semantic versioning conventions when creating new tags.

---

For any issues or questions, please contact the maintainers of this repository.
