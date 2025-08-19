# Node.js API Project

A simple REST API built with Node.js, TypeScript, and Fastify for managing courses.

## 🚀 Features

- **Fastify Framework**: High-performance web framework for Node.js
- **TypeScript**: Full TypeScript support with strict type checking
- **RESTful API**: Clean REST endpoints for course management
- **Logging**: Structured logging with Pino and pretty formatting
- **Modern ES Modules**: Uses ES2022+ features and Node.js 22

## 📋 Prerequisites

- Node.js 22 or higher
- npm or yarn package manager

## 🛠️ Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd "API Node.js"
```

2. Install dependencies:
```bash
npm install
```

## 🚀 Running the Application

### Development Mode
```bash
npm run dev
```

This will start the server with hot-reload using `ts-node-dev`.

### Production Mode
```bash
# Build the project
npx tsc

# Run the built JavaScript
node dist/server.js
```

## 🌐 API Endpoints

### GET /courses
Retrieve all available courses.

**Response:**
```json
{
  "courses": [
    { "id": "1", "title": "Curso de Node.js" },
    { "id": "2", "title": "Curso de React" },
    { "id": "3", "title": "Curso de React Native" }
  ]
}
```

### GET /courses/:id
Retrieve a specific course by ID.

**Parameters:**
- `id` (string): Course identifier

**Response:**
```json
{
  "course": {
    "id": "1",
    "title": "Curso de Node.js"
  }
}
```

**Error Response (404):**
```json
{}
```

### POST /courses
Create a new course.

**Request Body:**
```json
{
  "title": "Course Title"
}
```

**Response (201):**
```json
{
  "courseId": "generated-uuid"
}
```

**Error Response (400):**
```json
{
  "message": "Título obrigatório."
}
```

## 🏗️ Project Structure

```
API Node.js/
├── server.ts          # Main server file with API endpoints
├── package.json       # Project dependencies and scripts
├── tsconfig.json      # TypeScript configuration
├── docker-compose.yml # Docker configuration (empty)
└── requisicoes.http  # HTTP request examples
```

## 🛠️ Technologies Used

- **Fastify**: Web framework for Node.js
- **TypeScript**: Programming language with static typing
- **Pino**: Fast Node.js logger
- **ts-node-dev**: Development server with hot-reload
- **Node.js 22**: JavaScript runtime

## 📝 Development

### Scripts
- `npm run dev`: Start development server with hot-reload

### TypeScript Configuration
- Target: ES2022
- Module: NodeNext
- Strict mode enabled
- ES2024+ features support

## 🐳 Docker Support

The project includes a `docker-compose.yml` file for containerization (currently empty, ready for configuration).

## 📊 Server Information

- **Port**: 3333
- **Host**: localhost
- **Logging**: Pretty-formatted logs with timestamps

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the ISC License.

## 🆘 Support

For questions or issues, please open an issue in the repository.

---

**Note**: This is a learning project demonstrating Node.js API development with modern TypeScript practices.
