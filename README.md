# Local Supabase Setup Guide

This guide will help you set up a local Supabase instance for development.

## Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Git](https://git-scm.com/downloads)
- [Supabase CLI](https://supabase.com/docs/guides/cli)

## Setup Steps


1. **Start Docker Desktop**
   
   Ensure Docker Desktop is running before proceeding.


2. **Start Local Supabase Instance**

   ```bash
   npx supabase start
   ```

   This command will:
   - Pull necessary Docker images
   - Start the Supabase services
   - Create a local database
   - Output your local credentials

3. **Get Diff**
    ```bash
    npx supabase db diff -f initial_structure --db-url "postgresql://postgres.pltgbzgxnumanfhifaov:[password]@aws-0-us-east-1.pooler.supabase.com:6543/postgres"
    ```


## Important Local Credentials

After starting Supabase, you'll receive local credentials. Save these for your application:

- API URL: `http://localhost:54321`
- Database URL: `postgresql://postgres:postgres@localhost:54322/postgres`
- Studio URL: `http://localhost:54323`
- Inbucket URL: `http://localhost:54324`
- Default API Key: `your-anon-key`
- JWT Secret: `your-jwt-secret`

## Database Management 