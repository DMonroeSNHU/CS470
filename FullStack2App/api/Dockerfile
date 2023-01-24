

# using Node v12
FROM node:12

# Create app directory
WORKDIR /usr/src/lafs

#COPY --from=disk /usr/local/lib/docker* ./
# Copy 
# Install app dependencites
# a wildcard is used to unsure both package.json AND package-lock.json are copied
# where availavle (npm@5+)
COPY package*.json ./

RUN npm install

# If you are building your code for producation
# RUN npm ci --only=production

#Bundle app source
COPY  . .

# Expose port 3000 outside container
EXPOSE 3000

# Command used to start application
CMD ["node", "server/server.js"]

