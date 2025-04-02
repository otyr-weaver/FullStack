# ---- Stage 1: Build Stage ----
    FROM node:23 AS builder

    WORKDIR /app
    
    # Install dependencies
    COPY ./frontend/package.json ./frontend/package-lock.json ./
    RUN npm install
    
    # Copy app source code
    COPY ./frontend ./
    
    # Build Next.js app (optimized for production)
    RUN npm run build
    
    # ---- Stage 2: Production Server ----
    FROM node:23 AS runner
    
    WORKDIR /app
    
    # Copy only the necessary build output
    COPY --from=builder /app/.next .next
    COPY --from=builder /app/package.json package.json
    COPY --from=builder /app/public public
    
    # Install only production dependencies
    COPY --from=builder /app/node_modules node_modules
    
    # Expose the app port (default Next.js runs on 3000)
    EXPOSE 3000
    
    # Start Next.js in production mode
    CMD ["node_modules/.bin/next", "start"]
    