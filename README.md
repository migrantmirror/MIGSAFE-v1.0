# MIGSAFE-v1.0
Migrant Safety Framework &amp; Engine
import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Select, SelectItem } from "@/components/ui/select";

export default function HomePage() {
  return (
    <div className="min-h-screen bg-gray-50 p-6 space-y-8">
      <header className="text-center space-y-2">
        <h1 className="text-4xl font-bold text-green-700">MIGSAFE</h1>
        <p className="text-lg text-gray-700">Safe Steps. Stronger Journey.</p>
        <div className="flex justify-center space-x-4">
          <Select className="w-40" aria-label="Language Selector">
            <SelectItem value="en">English</SelectItem>
            <SelectItem value="ar">Arabic</SelectItem>
            <SelectItem value="fr">French</SelectItem>
            <SelectItem value="ha">Hausa</SelectItem>
          </Select>
        </div>
      </header>

      <section className="grid gap-6 md:grid-cols-2">
        <Card className="shadow-lg rounded-2xl">
          <CardContent className="space-y-4">
            <h2 className="text-2xl font-semibold text-green-800">Start Your Safety Guide</h2>
            <Input placeholder="Country of Origin" required aria-label="Country of Origin" />
            <Input placeholder="Destination Country" required aria-label="Destination Country" />
            <Input placeholder="Job Type (e.g., Domestic Worker)" required aria-label="Job Type" />
            <Button className="w-full bg-green-600 hover:bg-green-700" aria-label="Generate Checklist">Generate Checklist</Button>
          </CardContent>
        </Card>

        <Card className="shadow-lg rounded-2xl">
          <CardContent className="space-y-4">
            <h2 className="text-2xl font-semibold text-green-800">Verify a Job or Agent</h2>
            <Input placeholder="Agent Name or Job Offer ID" required aria-label="Job or Agent Verification" />
            <Button className="w-full bg-yellow-600 hover:bg-yellow-700" aria-label="Check for Red Flags">Check for Red Flags</Button>
          </CardContent>
        </Card>
      </section>

      <section className="grid gap-6 md:grid-cols-2">
        <Card className="shadow-md rounded-2xl">
          <CardContent className="space-y-4">
            <h2 className="text-xl font-semibold text-gray-800">Emergency Contacts</h2>
            <p className="text-gray-600">Quick access to helplines, embassies, and shelters by country.</p>
            <Button className="bg-red-600 hover:bg-red-700" aria-label="Open Emergency Support">Open Emergency Support</Button>
          </CardContent>
        </Card>

        <Card className="shadow-md rounded-2xl">
          <CardContent className="space-y-4">
            <h2 className="text-xl font-semibold text-gray-800">Report a Scam or Abuse</h2>
            <Textarea placeholder="Describe what happened..." required aria-label="Scam Report" />
            <Button className="bg-gray-700 hover:bg-black" aria-label="Submit Report">Submit Report</Button>
          </CardContent>
        </Card>
      </section>

      <section className="grid gap-6 md:grid-cols-2">
        <Card className="shadow-md rounded-2xl">
          <CardContent className="space-y-4">
            <h2 className="text-xl font-semibold text-blue-800">MIGSAFE AI Assistant</h2>
            <p className="text-gray-600">Ask questions about safety, jobs, legal issues, or travel advice in your language.</p>
            <Input placeholder="Ask your question here..." required aria-label="AI Assistant Input" />
            <Button className="bg-blue-600 hover:bg-blue-700" aria-label="Ask MIGSAFE">Ask MIGSAFE</Button>
          </CardContent>
        </Card>

        <Card className="shadow-md rounded-2xl">
          <CardContent className="space-y-4">
            <h2 className="text-xl font-semibold text-gray-800">Latest News & Blog</h2>
            <p className="text-gray-600">Updates on migration policies, success stories, and expert safety tips.</p>
            <Button className="bg-green-500 hover:bg-green-600" aria-label="Read Articles">Read Articles</Button>
          </CardContent>
        </Card>
      </section>

      <footer className="text-center text-sm text-gray-500 pt-8">
        &copy; 2025 MIGSAFE | Empowering Migrants, Preventing Exploitation
      </footer>
    </div>
  );
}
