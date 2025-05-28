import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { useState } from "react";
import { motion } from "framer-motion";

export default function PulsePointHome() {
  const [email, setEmail] = useState("");

  return (
    <main className="min-h-screen bg-gradient-to-b from-blue-100 to-white p-6">
      <section className="max-w-5xl mx-auto text-center py-20">
        <motion.h1
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}
          className="text-5xl font-bold text-blue-800 mb-6"
        >
          PulsePoint: Your Digital Life, In Tune
        </motion.h1>
        <p className="text-lg text-blue-700 mb-8">
          A wellness-focused social platform for ethical, mindful, and meaningful digital living.
        </p>
        <div className="flex justify-center gap-4">
          <Button className="px-6 py-3 text-lg">Get Early Access</Button>
          <Button variant="outline" className="px-6 py-3 text-lg">
            Learn More
          </Button>
        </div>
      </section>

      <section className="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-6xl mx-auto py-12">
        <Card className="shadow-xl rounded-2xl p-4">
          <CardContent>
            <h2 className="text-2xl font-semibold mb-2">Digital Pulse Dashboard</h2>
            <p>Track your screen time, privacy settings, and emotional tone in real-time.</p>
          </CardContent>
        </Card>
        <Card className="shadow-xl rounded-2xl p-4">
          <CardContent>
            <h2 className="text-2xl font-semibold mb-2">Ethical Content Planner</h2>
            <p>Plan posts with built-in copyright, tone, and accessibility checks.</p>
          </CardContent>
        </Card>
        <Card className="shadow-xl rounded-2xl p-4">
          <CardContent>
            <h2 className="text-2xl font-semibold mb-2">Footprint Cleaner</h2>
            <p>Scan and clean your digital trail across platforms.</p>
          </CardContent>
        </Card>
        <Card className="shadow-xl rounded-2xl p-4">
          <CardContent>
            <h2 className="text-2xl font-semibold mb-2">Pulse Circles</h2>
            <p>Join respectful, creative spaces to collaborate and learn responsibly.</p>
          </CardContent>
        </Card>
      </section>

      <section className="bg-blue-50 py-12">
        <div className="max-w-2xl mx-auto text-center">
          <h2 className="text-3xl font-bold mb-4 text-blue-800">Join Our Early Access List</h2>
          <p className="mb-6 text-blue-700">
            Be the first to experience a healthier, more ethical way to connect online.
          </p>
          <div className="flex flex-col sm:flex-row gap-4 justify-center">
            <Input
              placeholder="Enter your email"
              value={email}
              onChange={(e) => setEmail(e.target.value)}
              className="w-full sm:w-2/3"
            />
            <Button className="w-full sm:w-auto">Notify Me</Button>
          </div>
        </div>
      </section>
    </main>
  );
}---
id: updating-to-new-releases
title: Updating to New Releases
---

Create React App is divided into two packages:

- `create-react-app` is a global command-line utility that you use to create new projects.
- `react-scripts` is a development dependency in the generated projects (including this one).

When you run `npx create-react-app my-app` it automatically installs the latest version of Create React App.

> If you've previously installed `create-react-app` globally via `npm install -g create-react-app`, please visit [Getting Started](getting-started.md) to learn about current installation steps.

Create React App creates the project with the latest version of `react-scripts` so you’ll get all the new features and improvements in newly created apps automatically.

To update an existing project to a new version of `react-scripts`, [open the changelog](https://github.com/facebook/create-react-app/blob/main/CHANGELOG.md), find the version you’re currently on (check `package.json` in this folder if you’re not sure), and apply the migration instructions for the newer versions.

In most cases bumping the `react-scripts` version in `package.json` and running `npm install` (or `yarn install`) in this folder should be enough, but it’s good to consult the [changelog](https://github.com/facebook/create-react-app/blob/main/CHANGELOG.md) for potential breaking changes.

We commit to keeping the breaking changes minimal so you can upgrade `react-scripts` painlessly.
