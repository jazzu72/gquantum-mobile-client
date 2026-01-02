# gquantum-mobile-client

Quantum circuit execution client for AWS Braket & Qiskit - React Native iOS/Android mobile app.

## Features

- ✅ Quantum circuit design & visualization
- ✅ AWS Braket integration for quantum simulation
- ✅ Qiskit circuit support
- ✅ Real-time circuit execution
- ✅ Job status tracking and result visualization
- ✅ Cross-platform support (iOS & Android)
- ✅ Responsive UI with Tamagui/Tailwind
- ✅ State management with Zustand

## Prerequisites

- Node.js 18+
- npm or yarn
- React Native CLI
- Expo CLI (for easier setup)
- AWS Account (for Braket API access)
- Qiskit Python backend (optional)

## Project Structure

```
gquantum-mobile-client/
├── android/                  # Auto-generated (React Native)
├── ios/                      # Auto-generated
├── src/
│   ├── api/                  # API clients
│   │   ├── quantum.ts        # Braket/Qiskit API calls
│   │   └── auth.ts           # Authentication logic
│   ├── components/           # Reusable UI components
│   │   ├── QuantumCircuitVisualizer.tsx
│   │   └── ResultCard.tsx
│   ├── screens/              # Feature screens
│   │   ├── HomeScreen.tsx
│   │   ├── RunCircuitScreen.tsx
│   │   └── ResultsScreen.tsx
│   ├── navigation/           # React Navigation setup
│   ├── store/                # Zustand stores
│   │   └── quantumStore.ts   # Circuit state, job IDs, results
│   ├── utils/                # Helpers & constants
│   │   └── quantumHelpers.ts # Utility functions
│   ├── assets/               # Images, fonts
│   └── theme/                # Tamagui/Tailwind theme
├── App.tsx                   # Entry point
├── app.json                  # Expo config
├── babel.config.js
├── metro.config.js
├── package.json
├── tsconfig.json
├── .gitignore
└── .github/
    └── workflows/
        └── ci.yml            # CI workflow
```

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/jazzu72/gquantum-mobile-client.git
   cd gquantum-mobile-client
   ```

2. **Install dependencies:**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables:**
   Create a `.env` file in the root directory:
   ```env
   EXPO_PUBLIC_BRAKET_API_KEY=your_aws_braket_api_key
   EXPO_PUBLIC_BRAKET_REGION=us-east-1
   EXPO_PUBLIC_API_BASE_URL=https://api.example.com
   ```

4. **Start the development server:**
   ```bash
   npm start
   # or with Expo
   expo start
   ```

5. **Run on iOS:**
   ```bash
   npm run ios
   ```

6. **Run on Android:**
   ```bash
   npm run android
   ```

## Development

### Building the app

```bash
# Build for iOS
npm run build:ios

# Build for Android
npm run build:android
```

### Running tests

```bash
npm test
```

### Code formatting

```bash
npm run format
```

## API Integration

### AWS Braket
The app communicates with AWS Braket for quantum circuit execution. Ensure your AWS credentials are properly configured.

### Qiskit
Optional local Qiskit backend support for circuit simulation.

## Technologies Used

- **React Native** - Cross-platform mobile framework
- **Expo** - Development and deployment platform
- **TypeScript** - Type-safe development
- **Zustand** - Lightweight state management
- **Tamagui** - Cross-platform UI framework
- **React Navigation** - Navigation library
- **AWS SDK** - Braket API integration

## Troubleshooting

### Build Issues
- Clear cache: `expo start --clear`
- Reinstall dependencies: `rm -rf node_modules && npm install`

### API Connection Issues
- Verify AWS credentials in `.env`
- Check network connectivity
- Ensure API endpoints are accessible

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

MIT License - see LICENSE file for details

## Support

For issues and questions, please open a GitHub issue or contact the development team.

## Roadmap

- [ ] Advanced circuit optimizer
- [ ] Multi-device synchronization
- [ ] Hardware performance metrics
- [ ] Circuit library sharing
- [ ] Real quantum hardware execution
- [ ] Custom gate definitions
- [ ] Circuit export to QASM/OpenQASM
